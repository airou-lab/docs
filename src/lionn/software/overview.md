# Software

In short, the software stack consists of two devices, the VOXL and the NUC, connected via Ethernet so that ROS can communicate between devices.

## Main Software Components

### PX4 Platform

The VOXL Flight's software stack is based on the PX4 flight stack. For a beginner guide, see [this guide by PX4](https://docs.px4.io/main/en/getting_started/px4_basic_concepts.html).

In short, this bundle includes the following
* PX4 Autopilot
* QGroundControl (QGC)
* MAVSDK (communication between QGC and flight controller using MAVLink protocol)

### ROS

ROS is a flexible software framework to allow different compartmentalized processes for robotics.

### PANTHER

The Planner software is based on the [MIT-ACL's PANTHER](https://github.com/mit-acl/panther).

## Software Versions

### Operating Systems

The VOXL Flight uses the system image for SDK version `V0.9.5`, loaded onto the VOXL using the [SDK Upgrade instructions](https://docs.modalai.com/flash-system-image/).

The NUC is flashed with the minimized `Ubuntu 22.04 Server` image. This means the NUC is running headless (i.e. without a desktop interface).

### ROS
The NUC uses `ROS 2 Iron` while the VOXL's image (see OS section) comes bundled with `ROS Indigo`. The two versions typically are not compatible, but the two can communicate using the [ROS Bridge](https://docs.ros.org/en/iron/How-To-Guides/Using-ros1_bridge-Jammy-upstream.html).