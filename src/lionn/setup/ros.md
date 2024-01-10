# Setup ROS

Once the drone's networking infrastructure is established, we can set up ROS.

## Setup ROS on VOXL

[This guide](https://docs.modalai.com/setup-ros-on-voxl-0_9/) was used to setup ROS on the VOXL.

Specifically, the following values were set in the `my_ros_env.sh` on the VOXL:

```sh
export ROS_IP=10.0.0.20                                # VOXL Static IP
export ROS_MASTER_IP=10.0.0.10                         # NUC Static IP
export ROS_MASTER_URI=https://${ROS_MASTER_IP}:11311/  # ROS URI on NUC
```

## Setup ROS on the NUC

## MAVROS

MAVROS is used to send MAVLink commands (i.e. flight commands) from a ROS node to the VOXL's PX4 Flight controller.

First, MAVROS comes preinstalled on the VOXL but the NUC will need to have MAVROS installed.

ModalAI provide a `mavros_test` node to fly in a figure 8, which can be done using [this tutorial](https://docs.modalai.com/mavros-0_9/).

You may need to [configure the NUC to run the ROS Nodes on boot](https://mshields.name/blog/2022-03-16-running-ros-nodes-on-boot/).