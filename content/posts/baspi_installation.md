
+++
title = 'The BASpi - A Configurable BACnet Raspberry Pi Hat'
date = 2022-07-14T07:07:07+01:00
draft = false
+++

The BASpi is a raspberry pi HAT that can turn your raspbery pi into a configurable BACnet device. BACnet devices are used in commercial HVAC building automation. It is how large commercial buildings are able to trigger during a certain time of day or trigger from another sensor. For example, a BACnet devices can be used for turning down and turning up building air conditioning during certain times of day or year. It can be used for triggering a ventilator when smoke is detected.

BACnet are doing a lot of the building automation in the background that you didn't even know about. Since ICS devices are going more and more towards smart devices these devices are now going over protocols such as ethernet or even IoT protocols such as Zigbee. Here is a look at the BASpi I picked up:

![Alt text](/images/BASpi.jpg "BASpi Device")

This was my first project I took on that was an industrial or commercial IoT device and how these devices worked. This BASpi was good introduction into how BACnet protocol works and they operate. This BASpi can be purchased here at the URL:

<https://www.ccontrols.com/basautomation/baspi.php>

-----

## BASpi Points Types Specifications

When set up the BASpi acts a server allowing for both physical and virual points to be reached and communicated with. The following points are created when the BASpi server is running:

- 12 physical points:
  - 6 Analog Input (0-10V), Binary Input, Resistance, Thermistor (10KT2, 10KT3, 20K), Pulse Input max (40Hz).
  - 6 Six Relay Outputs (2A max current) or Four Relay and Two Analog Outputs (0-10 V).
- 24 virtual points:
  - 24 Virtual Points used to read or write data to/from wire sheet by a BACnet client/supervisor station
- 48 Web Components - allow live monitoring and forcing of wire sheet points from the BASpi's web page

-----

## BASpi Setup Guide

Comtemporary Controls list of references for hardware and software installation.

- [BASpi Home](https://www.ccontrols.com/basautomation/baspi.php "Hardware Installation")
- [BASpi Hardware Installation](https://www.ccontrols.com/pdf/BASpi-hardware-install-guide.pdf "Hardware Installation")
- [BASpi Software Installation](https://www.ccontrols.com/pdf/is/BASPI-soft-install-guide.pdf "Hardware Installation")
- [BASpi Image/Firmware Files](https://www.ccontrols.com/basautomation/baspisoftware.htm "Hardware Installation")

------

### Hardware Requirements

- BASpi HAT
- Raspberry Pi 3 or 4
- 8GB or larger micro SD card
- micro SD card to USB adapter

------

### Software Requirements

Two Software Installation types:

- Method A - Flash a Micro SD with pre-built Raspbian OS image and BASpi firmware already installed.
- Method B - Install BASpi firmware files to an already running Raspbian OS.

------

### Steps I did with Installation Method A

1. Power OFF the Raspberry Pi.
2. Mount the BASpi-IO hat on GPIO pins 1-10 on your Raspberry Pi as shown in the images here.
3. Download the BASpi image. <https://www.ccontrols.com/basautomation/baspisoftware.htm> (Make sure to select the right BASpi hat you have purchased. I had purchesd the BASpi-IO6U6R)
4. Place the Micro SD into the USB adapter and then connect to external computer.
5. Use Raspberry Pi Imager, <https://www.raspberrypi.com/software/>, to flash your Raspberry pi Micro SD card.
6. Select the custom operating system option at the bottom for the Rasperry imager to point to the image downloaded earlier.
7. Place Micro SD into the Raspberry pi.
8.  Turn ON the raspberry pi.
9.  Connect the raspberry pi to the internet via wireless or ethernet.
10. Find it's IP address by doing a `ifconfig` command in the terminal.
11. From an external computer connect to the IP address given to the raspberry pi. There you will see the interface of the BASpi server.
13. Type in User Name: admin, Password: admin.
14. Now should see the BASpi server interface.

After all is installed and it working properly, it is time to start playing around with the device.