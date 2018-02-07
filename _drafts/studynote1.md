---
layout: post
title:  Install ROS for Ubuntu Mate on Raspberry Pi 3
categories: Study
tags: [Ubuntu,Raspberry Pi,ROS]
---

Install ros for ubuntu mate on raspberry pi

System -> Administration -> Software & Updates
main,restricted,universe,and multiverse
Terminal:
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

for python3 to use ros

```shell
pip3 install pyyaml rospkg catcin_pkg

```

to use rosserial
```shell
sudo apt-get install ros-indigo-rosserial-arduino
sudo apt-get install ros-indigo-rosserial
```
