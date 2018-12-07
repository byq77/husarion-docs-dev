---
title: 'Using CORE2 with Mbed OS'
platform: 'CORE2'
autotoc: true
layout: layout.hbs
page: 'Tutorials'
order: 5
---

# Using CORE2 with Mbed OS

## Introduction

<div>
<center><img src="./../../../assets/img/mbed-tutorials/logo.png" width="600px" alt="Mbed OS logo"/></center>
</div>

**Mbed OS** is free, open-source platform and embedded operating system designed for IoT devices based on Arm Cortex-M family of microcontrollers. It is developed as collaborative project by *Arm*, its partners and growing community of individual devs from across the world. Mbed OS is distributed under the [Apache-2.0 License](https://en.wikipedia.org/wiki/Apache_License) and it's available on project's GitHub page : https://github.com/ARMmbed/mbed-os.

Besides support for variety of boards from different manufacturers the framework has the following features:
* built-in support for connectivity options like *Bluetooth LE*, *Wi-Fi*, *Ethernet*, *Cellular*, *LoRa LPWAN*, *NFC* and others,
* RTOS core based on open-source *CMSIS-RTOS RTX* (it is also possible to build projects without it),
* *Hardware Enforced Security* and *Communications Security*.

You can learn more about Mbed OS on its [official webpage](https://www.mbed.com/en/platform/mbed-os/).

## CORE2 and Mbed OS

In this tutorial we will show you how to build, compile and run mbed applications on CORE2 using mbed offline tools. You will be introduced to mbed API, learn how to use rosserial library to connect your mbed application with SBC and more. Let's hack ;-)

### Prerequisites

#### Hardware

You will need *ST-LINK V2 programmer* to flash CORE2 with mbed firmware.

#### Software

Before we start make sure you have following tools installed on your system:

* [Visual Studio Code IDE](https://code.visualstudio.com/)
* [GNU Arm Embedded version 6 toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)
* [STM32 ST-LINK Utility](https://www.st.com/en/development-tools/stsw-link004.html) (Windows only)
* [stlink flasher](https://github.com/texane/stlink/blob/master/README.md) (Mac or Linux)

You can check our tutorial: [2. Offline development tools](https://husarion.com/core2/tutorials/other-tutorials/offline-development-tools) to find information on stlink flasher and VS Code IDE installation and configuration. 

Everything up and ready? Proceed to the next step then.

### mbed-cli installation

`mbed-cli` is a package name of **Arm Mbed CLI**, a command-line tool that enables use of Mbed build system, GIT/Mercurial-based version control, dependencies management and so on. Check it [GitHub page](https://github.com/ARMmbed/mbed-cli) to learn more about the tool. 

Official mbed documentation provides tutorial on mbed-cli installation. You can access it [here](https://os.mbed.com/docs/v5.10/tools/installation-and-setup.html).
It provides installers for both Windows and macOS. Linux users will need to install the tool manually.

To check if installation was successful open terminal and run:

```bash
    $ mbed --version
    1.8.3
```

After installation you have to inform Mbed CLI about location of compiler (in our case GCC Arm Embedded Compiler ). We will use global setting. Run:

```bash
    $mbed config -G GCC_ARM_PATH <path to compiler>
```

Example for Linux:


```
$ where arm-none-eabi-gcc # prints path to arm-none-eabi-gcc.exe if in PATH
$ mbed config -G GCC_ARM_PATH "C:\Program Files (x86)\GNU Tools ARM Embedded\6 2017-q2-update\bin" # configure path for mbed-cli
$ mbed config --list # check configuration
```

$ mbed 

## Motor project

## Rosserial project

## Summary

After completing this tutorial you should know what are the basic
components and tools of ROS. You should know two methods for starting a
node, setting parameters and remapping topic names. You should be able
to check what nodes are running in system and to which topics they are
publishing and subscribing.

---------

*by Szymon Szantula, Husarion*

*Do you need any support with completing this tutorial or have any difficulties with software or hardware? Feel free to describe your thoughts on our community forum: https://community.husarion.com/ or to contact with our support: support@husarion.com*