# Setup ROS

## Setup ROS on VOXL

[This guide](https://docs.modalai.com/setup-ros-on-voxl-0_9/) was used to setup ROS on the VOXL.

Specifically, the following values were set in the `my_ros_env.sh` on the VOXL:

```bash
ROS_IP=10.0.0.20                            # VOXL Static IP
ROS_MASTER_IP=10.0.0.10                     # NUC Static IP
ROS_MASTER_URI=https://$ROS_MASTER_IP:22222 # ROS URI on NUC
```

## Setup ROS on the NUC