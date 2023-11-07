# Starter Guide

## Connecting to the VOXL

ModalAI provides a [Developer Bootcamp for the VOXL](https://docs.modalai.com/voxl-developer-bootcamp/) which contains lots of useful information and the basic setup steps we used.

Developers may connect to the VOXL in one of two ways:

### Wired via microUSB using ADB

Be sure to connect using the built-in microUSB port, not the USB extension.

0. Assure the VOXL is powered on.
1. Connect the VOXL and developer machine using microUSB-to-USB-A cable.
2. Run `adb`

For more information, see the [VOXL adb setup guide](https://docs.modalai.com/setting-up-adb/).

### Wireless using Wi-Fi using SSH

The VOXL Flight transmits a Wi-Fi network for use in development.

0. Assure the VOXL is powered on.
1. First, connect to the wireless network (named `voxl-wifi`) using the default password `1234567890`.
2. To SSH into the VOXL, run `ssh root@192.168.8.1`, providing the default password `oelinux123`.

For more information, see the [VOXL wifi setup guide](https://docs.modalai.com/voxl-wifi-setup/).

### Web Interface

The VOXL will transmit a web interface summarizing the VOXL's information and giving camera previews.

When connected to the VOXL's WLAN, this web interface can be found at <http://192.168.8.1/> in the web browser.

For more information, see the [VOXL Portal guide](https://docs.modalai.com/voxl-portal/)

### QGroundControl

Our development PC is configured to automatically connect to the VOXL's QGC server when connected to `voxl-wifi` and QGC is opened.

You can also connect to QGC via the microUSB extension cord (VOXL usb-jst) plugged into the [Flight Core's USB connector](https://docs.modalai.com/voxl-flight-datasheet-connectors/#j1006---usb-connector). This USB connector doesn't connect to the Linux OS on the VOXL, instead connecting directly to the PX4.

For more information, see the [VOXL QGC connection guide](https://docs.modalai.com/qgc-wifi/)