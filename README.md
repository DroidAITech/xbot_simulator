# xbot_simulator
===================

Launchers for Gazebo and stage simulation of the XBot

## 安装所需依赖

1. xbot源码包；

```
https://yt.droid.ac.cn/xbot-u/xbot/-/tree/melodic-devel
```
2. 编译运行所需依赖，根据具体问题，安装对应的ros包，也可以使用进行初步：

```
 cd ~/catkin_ws
 rosdep install --from-paths src --ignore-src --rosdistro=melodic -y      #默认18.04
```

如果出现找不到相关包，还需要单独安装：

```
sudo apt-get install ros-melodic-package-name
```

## 启动gazebo仿真

启动仿真环境

```
roslaunch xbot_gazebo xbot_world.launch
```

启动gmapping（要求仿真环境已经启动，下同）

```
roslaunch xbot_gazebo gmapping_demo.launch
```

启动rviz，观察建图

```
cd ~/YOUR_PATH/xbot_gazebo/rviz
rviz -d gmapping.rviz
```

## 启动stage仿真

```
roslaunch xbot_stage xbot_in_stage.launch
```