ROSBot control mode development 

Инструкция по работе

```
1. install ROS Melodic (ros-melodic-desktop-full)

    http://wiki.ros.org/melodic/Installation/Ubuntu
    sudu apt install python-catkin-tools - вроде бы должны ставиться вместе с ROS, но нет.

2.  Create catkin ws

    cd path_to_ws
    mkdir -p catkin_ws/src
    cd catkin_ws
    wstool init ./src
    cd src
    git clone https://github.com/urock/rosbot.git   - изменил ссылку
    cd ..
    sudo apt update
    rosdep install --from-paths src --ignore-src -r -y  
    catkin build


3. Run smth

    cd ~/work/rosbot/catkin_ws
    source devel/setup.zsh
    roslaunch rosbot2 urock_system.launch
    roslaunch rosbot_controller folow_path.launch 

```

