---
title: Monitoring
categories:
  - Docker
tags:
  - 手札
  - 程設
date: 2026-08-12 14:26:40
---
使用 **Prometheus** 搭配 **Grafana**、**Node Exporter**（收集 CPU/RAM/Disk/Network）與官方 **NVIDIA DCGM Exporter**（收集 GPU 狀態）是目前企業級與 AI 訓練伺服器監控的最標準做法。

1. **確認前置環境 (NVIDIA Container Toolkit):** 若無 GPU 存取權限，DCGM 容器將無法啟動.
容器需要透過 NVIDIA Container Toolkit 存取宿主機的 GPU 驅動。若尚未安裝，請先在 Ubuntu 執行以下指令安裝並重啟 Docker：

```bash
# 安裝 NVIDIA Container Toolkit
sudo apt-get update
sudo apt-get install -y nvidia-container-toolkit

# 設定 Docker Runtime 並重啟服務
sudo nvidia-ctk runtime configure --runtime=docker
sudo systemctl restart docker

```


2. **建立專案目錄結構:**
建立專用的監控目錄與 Prometheus 設定檔夾：

```bash
mkdir -p ~/gpu-monitoring/prometheus
cd ~/gpu-monitoring

```


3. **建立 Prometheus 設定檔 (prometheus.yml):**
建立 `prometheus/prometheus.yml` 檔案，指定抓取資料的時間間隔與 Target：

```bash
nano prometheus/prometheus.yml

```

將以下內容貼入檔案中：

```yaml
global:
  scrape_interval: 15s      # 資料抓取頻率
  evaluation_interval: 15s

scrape_configs:
  - job_name: 'node-exporter'
    static_configs:
      - targets: ['node-exporter:9100']

  - job_name: 'dcgm-exporter'
    static_configs:
      - targets: ['dcgm-exporter:9400']

```


4. **建立 Docker Compose 設定檔 (docker-compose.yml):**
在 `~/gpu-monitoring` 目錄下建立 `docker-compose.yml` 檔案：

```bash
nano docker-compose.yml

```

貼入以下設定：

```yaml
version: '3.8'

services:
  prometheus:
    image: prom/prometheus:v2.51.0
    container_name: prometheus
    restart: unless-stopped
    ports:
      - "9090:9090"
    volumes:
      - ./prometheus/prometheus.yml:/etc/prometheus/prometheus.yml
      - prometheus_data:/prometheus
    command:
      - '--config.file=/etc/prometheus/prometheus.yml'
      - '--storage.tsdb.path=/prometheus'

  grafana:
    image: grafana/grafana:10.4.0
    container_name: grafana
    restart: unless-stopped
    ports:
      - "3000:3000"
    volumes:
      - grafana_data:/var/lib/grafana

  node-exporter:
    image: prom/node-exporter:v1.7.0
    container_name: node-exporter
    restart: unless-stopped
    ports:
      - "9100:9100"
    volumes:
      - /proc:/host/proc:ro
      - /sys:/host/sys:ro
      - /:/rootfs:ro
    command:
      - '--path.procfs=/host/proc'
      - '--path.sysfs=/host/sys'
      - '--path.rootfs=/rootfs'

  dcgm-exporter:
    image: nvcr.io/nvidia/k8s/dcgm-exporter:3.3.5-3.4.0-ubuntu22.04
    container_name: dcgm-exporter
    restart: unless-stopped
    ports:
      - "9400:9400"
    deploy:
      resources:
        reservations:
          devices:
            - driver: nvidia
              count: all
              capabilities: [gpu]

volumes:
  prometheus_data:
  grafana_data:

```


5. **啟動服務與登入 Grafana:**
在 `~/gpu-monitoring` 目錄下啟動所有容器：

```bash
docker compose up -d

```

啟動後可透過以下 Port 驗證服務：

* **Grafana**: `http://<YOUR_SERVER_IP>:3000`（預設帳號/密碼為 `admin` / `admin`）
* **Prometheus**: `http://<YOUR_SERVER_IP>:9090`


6. **設定 Grafana 資料源與匯入儀表板:**
1. 開啟瀏覽器並登入 Grafana (`http://<YOUR_SERVER_IP>:3000`)。
2. 前往 **Connections** > **Data Sources** > 點擊 **Add data source**，選擇 **Prometheus**。
3. 在 **Prometheus server URL** 輸入 `http://prometheus:9090`，拉到最下方點擊 **Save & test**。
4. 前往 **Dashboards** > 點擊右上角 **New** > **Import**：
* 輸入 ID `1860` 匯入 **Node Exporter Full**（用於查看 CPU、RAM、Disk、Network 歷史圖表）。
* 輸入 ID `12239` 匯入 **NVIDIA DCGM Exporter Dashboard**（用於查看 GPU 使用率、VRAM、功耗與溫度）。
