RPLIDAR ROS package
=====================================================================

ROS node and test application for RPLIDAR

How to build rplidar ros package
=====================================================================
    1) Clone this project to your catkin's workspace src folder
    2) Running catkin_make to build rplidarNode and rplidarNodeClient

For GMapping SLAM on ROS, the laser scan message created by RPLIDAR node is modified to use a frame rotated by 180 degrees. Using this 
frame, the resulting min and max angle will be approximately equal to -3.14 and 3.14 according to GMapping condition.

scan_msg.angle_min =  M_PI - angle_min;
scan_msg.angle_max =  M_PI - angle_max;

