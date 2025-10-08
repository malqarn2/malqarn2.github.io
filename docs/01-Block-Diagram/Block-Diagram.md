---
title: Individal Block Diagram
tags:
- tag1
- tag2
---

## Overview
This block diagram shows how the AutoCan system works. It includes the main parts used for sensing, control, and movement. A 9 V DC power supply provides energy to the motor driver and also to a 5 V regulator that powers the sensors and the microcontroller. The light sensor detects brightness and sends an analog signal to the PIC18F57Q43 microcontroller. Two buttons provide user input. The microcontroller processes these signals and controls both the DC motor and a red LED using digital and PWM outputs. The motor driver (L293D) receives signals from the microcontroller to run the motor forward or backward. All parts are connected through digital and analog lines, allowing smooth communication between the sensors, controller, and actuators.

To get some initial formatting help, one can view ["here"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/Appendix/basic-markdown-examples/) some basic techniques.


## Example Block Diagram 
Showing an example of how to import a screenshot of the block diagram created outside of git and brought into a page.

![](individual-block-diagram.png)
