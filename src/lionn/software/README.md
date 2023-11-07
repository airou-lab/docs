# Software
Below is a description of the main components in the software architecture for the drone.

## PX4 Platform

The VOXL Flight's software stack is based on the PX4 flight stack. For a beginner guide, see [this guide by PX4](https://docs.px4.io/main/en/getting_started/px4_basic_concepts.html).

In short, this bundle includes the following
* PX4 Autopilot
* QGroundControl (QGC)
* MAVSDK (communication between QGC and flight controller using MAVLink protocol)

## ROS

ROS is a flexible software framework to allow different processes 

## PANTHER

The Planner software is based on the MIT-ACL's PANTHER.