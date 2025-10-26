---
title: Individal Block Diagram
---

## Overview
This block diagram shows how the AutoCan system controls the motion of the trash can lid using a DC motor. It includes the main components for power regulation, control, and actuation. A 9 V DC power supply provides energy to the motor driver and a 5 V regulator, which powers the microcontroller and supporting circuits.

The microcontroller (PIC18F57Q43 Curiosity Nano) reads input signals from the user via buttons and processes control logic to operate the motor. It sends control signals through digital I/O and PWM outputs to the motor driver (L293D), which drives the DC motor to open or close the lid.

To get some initial formatting help, one can view ["here"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/Appendix/basic-markdown-examples/) some basic techniques.


## Example Block Diagram 
Showing an example of how to import a screenshot of the block diagram created outside of git and brought into a page.

<img width="977" height="599" alt="Image" src="https://github.com/user-attachments/assets/d4c3f72a-98c1-4f66-963a-23ecb9912c6a" />
