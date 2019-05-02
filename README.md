# SARP-Bot
## Overview
SPARC Autonomous ROS Platform Robot (SARP-Bot).  SPARC's [IEEE SoutheastCon Hardware Competition 2019 robot](https://github.com/SPARC-Auburn/IEEE-SoutheastCon-2019) has great hardware for numerous robotics applications in a small form factor.  The practice bot will be revamped to support an electronics upgrade to allow more processor intensive computations.

## Original Approach
The robot utilizes two Raspberry Pi microcomputers to control the robot while using an attached camera to identify the color and shape of the objects on the field.  A LIDAR is used to localize the robot on the arena to help avoid the four lights and the wooden box in the middle of the arena.  The design of the robot is to move the objects to the appropriate home base by running over the objects, closing a small door on the front of the robot, hold them under the robot and move towards the appropriate home base of the object.  Figure 1 shows the competition robot design.

<img src="Images/Mechanical%20Development/final-bot.jpg"  width="400px"/>

**Figure 1:** Final robot design

## Modified Approach
The new design will utilize an Intel NUC instead of two Raspberry Pi's.  This will simplify the design as well as drastically increasing the processing capability of the robot.  This will involve a battery replacement to support the higher voltage requirement of the NUC.  It will also involve a complete revamping of the software in order to more elegantly and efficiently complete localization and navigational tasks.

## Technical Documentation
* [Mechanical](https://github.com/SPARC-Auburn/IEEE-SoutheastCon-2019/tree/master/Mechanical-Hardware)
* [Electrical Hardware](https://github.com/SPARC-Auburn/IEEE-SoutheastCon-2019/tree/master/Electrical-Hardware)
* [Software](https://github.com/SPARC-Auburn/SARP-Bot-Software)

