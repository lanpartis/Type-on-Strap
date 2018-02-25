---
layout: post
title: ROS beginner tutorial in short
tag: ROS
---

Requirement:
ROS installed.

## init environment

After installing ROS, we need to put the following instructions in `~/.bashrc file` to let shell automatically load environment variables.
```shell
source /opt/ros/<ros>/setup.bash
source <catkin_workspace>/devel/setup.bash
```

If you use zsh, change the setup.bash file to setup.zsh

## create workspace
```shell
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws
catkin_make
```

##create a ROS package
```shell
cd ~/catkin_ws/src
catkin_create_pkg <package_name> <depend1> <depend2>
```

## run ROS node
```shell
rosrun <package_name> <node_name>
```

##create a publisher/listener (in python)
