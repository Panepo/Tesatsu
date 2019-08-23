---
title: Turtlebot3 simulation
categories:
  - 手札
  - 程設
tags:
  - 手札
  - 程設
date: 2019-08-23 10:32:25
---
This is the note for set up development environment of Turtlebot3 simualtion on Ubuntu 16.04 LTS

1. Install command for dependent packages
```
sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-teleop-twist-joy ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-arduino ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation
```

2. Install Turtlebot3 packages
```
cd ~/catkin_ws/src/
git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
cd ~/catkin_ws && catkin_make
```

3. Set simulation parameters to ./bashrc
```
EXPORT TURTLEBOT3_MODEL=waffle
export ROS_HOSTNAME=localhost
export ROS_MASTER_URI=http://${ROS_HOSTNAME}:11311
```

4. Start SLAM and navigation simulation

  * Build the map by SLAM
  ```
  roslaunch turtlebot3_gazebo turtlebot3_world.launch
  roslaunch turtlebot3_gazebo turtlebot3_simulation.launch
  roslaunch turtlebot3_slam turtlebot3_slam.launch
  rosrun map_server map_saver -f ~/map
  ```

  * Start navigation
  ```
  roslaunch turtlebot3_gazebo turtlebot3_world.launch
  roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
  ```
