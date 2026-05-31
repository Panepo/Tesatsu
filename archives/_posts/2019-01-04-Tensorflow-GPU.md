---
title: Tensorflow-GPU
categories:
  - Machine Learning
tags:
  - 手札
  - 程設
date: 2019-01-04 16:18:01
---
This is the note for set up development environment of tensorflow-GPU with nvidia cuda.

1. Install Anaconda

  The python version I use is 3.6

2. Install Nvidia driver

  The driver version I use us 417.35

3. Install CUDA 9.0

  From now(2019/1/4), tensorflow supports CUDA 9.0. You may check the compatility via this {% link link https://www.tensorflow.org/install/gpu %}
  The download link is {% link here https://developer.nvidia.com/cuda-toolkit-archive %}. There are four patches but seems not needed.
<center>{% asset_img cuda.png cuda %}</center>

4. Install cuDNN 7.0 for CUDA 9.0

  From now(2019/1/4), tensorflow supports cuDNN 7.2. You may check the compatility via this {% link link https://www.tensorflow.org/install/gpu %}
  The download link is {% link here https://developer.nvidia.com/cudnn %}.
  <center>{% asset_img cudnn.png cudnn %}</center>
  When the downloading process is complete, extract the file and there are three folders inside cuda folder, move those three folders to CUDA install path.
  The default CUDA install path is `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0`

5. Set up system environment variables

  Add `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin` and `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\libnvvp` to your `PATH` in system variables.

6. Install tensorflow-gpu 1.11

  Current version of tensorflow is too new that we should install older version.
  `pip install tensorflow-gpu==1.11`

  Then verify if tensorflow-gpu is installed or not:
```
from tensorflow.python.client import device_lib
local_device_protos = device_lib.list_local_devices()
print(local_device_protos)
```
  If CPU and GPU are both detected as below, the installation is sucessfully.
```
tensorflow:1.11.0
[name: "/device:CPU:0"
device_type: "CPU"
memory_limit: 268435456
locality {
}
incarnation: 15352562079212995961
, name: "/device:GPU:0"
device_type: "GPU"
memory_limit: 3213551206
locality {
  bus_id: 1
  links {
  }
}
incarnation: 18385036426934203187
physical_device_desc: "device: 0, name: GeForce GTX 950M, pci bus id: 0000:01:00.0, compute capability: 5.0"
]
```
