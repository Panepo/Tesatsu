---
title: ROS2 environment
categories:
  - ROS
tags:
  - 手札
  - 程設
  - 轉錄
date: 2020-03-13 11:03:38
---
This is the note for set up development environment of ROS2 (robot operation system) Dashing Diademata on Ubuntu 18.04 LTS

1. Setup locale
```
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
```

2. Setup resource
```
sudo apt update && sudo apt install curl gnupg2 lsb-release
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo sh -c 'echo "deb http://packages.ros.org/ros2/ubuntu `lsb_release -cs` main" > /etc/apt/sources.list.d/ros2-latest.list'
```

3. Install ROS2 packages
```
sudo apt update
sudo apt install ros-dashing-desktop
```

4. Install additional libraries (optional)

- argcomplete
```
sudo apt install python3-argcomplete
```

- RMW implementations
```
sudo apt install ros-dashing-rmw-opensplice-cpp # for OpenSplice
sudo apt install ros-dashing-rmw-connext-cpp # for RTI Connext (requires license agreement)
```

- ROS1 bridge
```
sudo apt install ros-dashing-ros1-bridge
```

5. Install application for tutorial (optional)

- turtlesim
```
sudo apt install ros-dashing-turtlesim
```

- rqt
```
sudo apt install ros-dashing-rqt-*
```
