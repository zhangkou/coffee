ROS机器人测试
roslaunch clbrobot bringup.launch
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
roscd teleop_twist_keyboard

ROS机器人IMU校正
roslaunch clbrobot bringup.launch
rosrun imu_calib do_calib

ROS机器人线速度校正
roslaunch clbrobot bringup.launch
rosrun clbrobot_nav calibrate_linear.py
rosrun rqt_reconfigure rqt_reconfigure
roscd clbrobot
cd launch
nano bringup.launch

ROS机器人角速度校正
roslaunch clbrobot bringup.launch
rosrun clbrobot_nav calibrate_angular.py
rosrun rqt_reconfigure rqt_reconfigure
roscd clbrobot
cd launch
nano bringup.launch

ROS机器人SLAM建图
roslaunch clbrobot bringup.launch
roslaunch clbrobot lidar_slam.launch
rviz
cd /home/clbrobot/catkin_ws/src/clbrobot_project/clbrobot/maps
./map.sh

ROS机器人雷达导航自主规划与避障
roslaunch clbrobot bringup.launch
roslaunch clbrobot navigate.launch
rviz

























