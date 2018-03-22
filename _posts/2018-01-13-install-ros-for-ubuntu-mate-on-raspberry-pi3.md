---
layout: post
title:  Install ROS for Ubuntu Mate on Raspberry Pi 3
tags: [Ubuntu,Raspberry Pi,ROS]
---

**Requirement:**

Raspberry Pi just flashed with [Ubuntu Mate](https://ubuntu-mate.org/download/) image.

**First:**

Go to System -> Administration -> Software & Updates
make following chechboxes cheched:
main,restricted,universe,and multiverse

**Then**:

Go to Terminal:
```shell
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
wget http://packages.ros.org/ros.key -O - | sudo apt-key add -
sudo apt-get update
sudo apt-get install ros-kinetic-desktop-full
sudo rosdep init
rosdep update
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

**Extra:**

For Python3 to use ROS
```shell
pip3 install pyyaml rospkg catkin_pkg
```
To use rosserial to control Arduino
```shell
sudo apt-get install ros-kinetic-rosserial-arduino
sudo apt-get install ros-kinetic-rosserial
```
