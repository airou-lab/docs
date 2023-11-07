# Setup Guide
This document details the steps to implement the setup for the LIONN platform.

## Setup VOXL

The [VOXL Developer Bootcamp](https://docs.modalai.com/voxl-developer-bootcamp/) from ModalAI was used to setup the VOXL.

The latest VOXL image was loaded (see [Software](../software/README.md#operating-systems)) and the `voxl-configure-mpa` script to configure the different services on the VOXL based on the hardware shipped with the VOXL Flight Deck (see [voxl-configure-mpa](https://docs.modalai.com/voxl-configure-mpa/))

## Testing VOXL Motor connections

Two methods were used to test if the VOXL was able to control the propeller motors.

***Ensure the propellers are removed before testing!***

### Generate a PWM signal

The main method to test connections is using QGroundControl. Once connected (see [Software Starter Guide < QGroundControl](../software/starter.md#qgroundcontrol)) the QGroundControl app provides configuration for the drone. In the Motor tab, a test slider can be used to power up the motors.

Secondly, when unable to connect the VOXL to QGC, ModalAI provides a [Flight Core PWM ESC Calibration script](https://docs.modalai.com/flight-core-pwm-esc-calibration/) that can be used to bypass QGC.

### Test the PWM signal coming from the VOXL

In order to ensure the PWM connection was provided to the ESCs in the first place, a simple LED circuit was created and connected to the PWM output for one of the 6 motor outputs on the VOXL's PWM breakout board. The LED's ground pin was connected to the PWM ground, and the positive pin was connected to the PWM's power and signal pins.

When the signal was sent using one of the above methods, the LED would flash, indicating the PWM signal being successfully sent.

## Setup ROS on VOXL

[This guide](https://docs.modalai.com/setup-ros-on-voxl-0_9/) was used to setup ROS on the VOXL.

## Setup NUC

Enable wifi using `nmcli` and connect to the VOXL's wifi network.

[Enable the SSH server on the NUC](https://www.cyberciti.biz/faq/how-to-install-ssh-on-ubuntu-linux-using-apt-get/) and [configure the firewall](https://www.cyberciti.biz/faq/howto-configure-setup-firewall-with-ufw-on-ubuntu-linux/), enabling ssh connections (port 22). Ensure that in the `/etc/ssh/sshd_config` file, `PasswordAuthentication yes` exists as a line.

Now, once connected to the VOXL's wifi network, the developer computer can SSH into both the VOXL and the NUC.