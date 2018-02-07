---
layout: single
title:  "Draft Post"
header:
  teaser: "unsplash-gallery-image-2-th.jpg"
categories:
  - Study
tags:
  - edge case
---
Install ros for ubuntu mate on raspberry pi

System -> Administration -> Software & Updatesへ
main,restricted,universe,and multiverse
Terminal:
```shell

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
wget http://packages.ros.org/ros.key -O - | sudo apt-key add -
sudo apt-get update
sudo apt-get install ros-kinetic-desktop-full (ここでとても時間がかかるのでお出かけ推奨)
sudo rosdep init
rosdep update
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

for python3 to use ros

```shell
sudo apt-get install python3-rospkg
sudo apt-get install python3-catkin_pkg

```

to use rosserial
```shell
sudo apt-get install ros-indigo-rosserial-arduino
sudo apt-get install ros-indigo-rosserial
```
