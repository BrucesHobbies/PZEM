# PZEM
Python Interface to PZEM AC/DC Power / Energy Monitoring Modules

Copyright(C) 2021, BrucesHobbies,
All Rights Reserved

# PZEM Module Overview
PZEM.py provides a Python scripting interface to the Peacefair PZEM AC and DC energy / power monitoring modules. The module measures the following:
- voltage (V)
- amperage (A)
- power (W-Hr)
- freq (Hz)
- power factor
- state

![Figure 1: PZEM](https://github.com/BrucesHobbies/sumpMaster/blob/main/figures/figure1.png)

Consult an electrician for your local electrical codes. Also refer to the documentation that comes with the PZEM module. For devices powered off alternating house current, either 120 or 240 volt, the PZEM uses a split transformer to measure current through a wire. It is snapped around the neutral wire to sense the current flow. The module also requires connection to hot and neutral to measure the voltage being provided to the device. For Direct Current devices there is the PZEM-017 module.

![Figure 2: PZEM Wiring](https://github.com/BrucesHobbies/sumpMaster/blob/main/figures/figure2.png)

# Required Hardware 
As an Amazon Associate I earn a small commission from qualifying purchases. It does not in any way change the prices on Amazon. I appreciate your support, if you purchase using the links below.
## PZEM Module (about $20 USD)
For Alternating Current (AC) devices
- One of the following AC power PZEM-016 modules - may have different shipping times
  - [Amazon: PZEM-016](https://amzn.to/394y8VT)
  - [Amazon: PZEM-016](https://amzn.to/2PhmK1M)
  - [Amazon: PZEM-016](https://amzn.to/3lG36su)

For Direct Current (DC) devices
- One of the following DC power PZEM-017 modules - may have different shipping times
  - [Amazon: PZEM-017](https://amzn.to/315rXwv)

- 2-conductor low voltage wire as needed (RS-485 connection from PZEM module to USB dongle)

## Raspberry Pi system (if you don’t already own one)
- Raspberry Pi (any of the following)
  - [RPI-Zero]( https://amzn.to/3ly0mM0)
  - [RPI 3B+]( https://amzn.to/3lyPBJe)
  - [RPI 4B]( https://amzn.to/2Vwulto)
- Power adapter for your Raspberry Pi
- Heatsinks (optional)
- SD-Card


# Software Installation
## Step 1: Install the Raspberry Pi Operating System.
Here are the instructions to install the Raspberry Pi Operating System.
[Raspberry Software Install Procedure](https://www.raspberrypi.org/software/operating-systems/)

Before continuing make sure your operating system has been updated with the latest updates.

    sudo apt-get update
    sudo apt-get full-upgrade
    sudo reboot now


## Step 2: Download PZEM software
To get a copy of the source files type in the following git command assuming you have already installed git:

    git clone https://github.com/BrucesHobbies/PZEM

Download prerequisitie ModBus.

    sudo pip3 install pymodbus

Verify PZEM module presence using the RPi command line (once attached by USB cable and RS-485 cable with module power on):

    ls /dev/ttyUSB*    # Show USB devices
    lsusb -v           # Show USB devices with details

# Future Options
Please feel free to fork and contribute or provide feedback on priorities and features

# Test 
To perform a quick read of the PZEM module use the following command:

    python3 pzem.py

# Feedback
Let us know what you think of this project and any suggestions for improvements. Feel free to contribute to this open source project.
