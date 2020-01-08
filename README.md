VectorNav Ros drivers

A ROS node for VectorNav INS & GPS devices.

This package provides a sensor_msg interface for the VN100, 200, & 300
devices. Simply configure your launch files to point to the serial port
of the deice and you can use rostopic to quickly get running.   

QuickStart Guide
----------------

This assumes that you have a VectorNav device connected to your computer
via a USB cable.

How to run
1. roscore
2. Open vectornav.launch and change the yaml file for vn100 or vn200 respectively
3. roslaunch vectornav vectornav.launch
4. rostopic list
5. rostopic echo /vectornav/IMU
6. ctrl+c to quit


Overview
--------

#### vnpub node

This node provides a ROS interface for a vectornav device. It can be configured
via ROS parameters and pubishes sensor data via ROS topics.


#### vectornav.launch

This launch file contains the default parameters for connecting a device to ROS.
You will problaby want to copy it into your own project and modify as required.


References
----------

[1]: http://www.vectornav.com/ "VectorNav"
[2]: http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment "ROS Workspace Tutorial"
