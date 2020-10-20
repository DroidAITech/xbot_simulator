# xbot_simulator
===================

Launchers for Gazebo and stage simulation of the XBot

## 安装所需依赖

1. 下载xbot源码包；

```
git clone https://github.com/DroidAITech/xbot.git
```
2. 编译运行所需依赖，根据具体问题，安装对应的ros包，也可以使用一下命令进行初步安装：

```
 cd ~/catkin_ws
 rosdep install --from-paths src --ignore-src --rosdistro=kinetic -y      #默认16.04
```

如果编译还出现找不到相关包，还需要单独安装：

```
sudo apt-get install ros-kinetic-package-name
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
启动机器人键盘控制程序

```
rosrun xbot_gazebo  robot_keyboard_teleop.py 
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
