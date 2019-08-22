---
title: ROS environment
categories:
  - 手札
  - 程設
tags:
  - 手札
  - 程設
date: 2019-08-22 13:32:18
---
This is the note for set up development environment of ROS (robot operation system) on Ubuntu 16.04 LTS

1. NTP(Network Time Protocol) Configuration (Optional)
```
sudo apt-get install -y chrony ntpdate
sudo ntpdate -q ntp.ubuntu.com
```

2. Adding Source List
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

3. Setting up the Key
```
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
```

4. Updating the Package Index
```
sudo apt-get update && sudo apt-get upgrade -y
```

5. Installing ROS Kinetic Kame
```
sudo apt-get install ros-kinetic-desktop-full
sudo apt-get install ros-kinetic-rqt*
```

6. Initializing rosdep
```
sudo rosdep init
rosdep update
```

7. Installing rosinstall
```
sudo apt-get install python-rosinstall
```

8. Load the Environment File
```
source /opt/ros/kinetic/setup.bash
```

9. Creating and Initializing a Workspace Folder
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
catkin_init_workspace
cd ~/catkin_ws/
catkin_make
```

10. Load the Environment File
```
source ~/catkin_ws/devel/setup.bash
```

Remember to put 8 and 10 to .bashrc file.
