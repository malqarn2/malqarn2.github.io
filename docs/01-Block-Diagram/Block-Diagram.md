---
title: Individal Block Diagram
---

## Overview
This block diagram illustrates how the AutoCan motor control system operates using a Microchip PIC18F57Q43 Curiosity Nano board. The system controls a 6V N20 DC motor through a custom-built H-Bridge made of FAN8100, enabling bidirectional motor rotation.

An op-amp (MCP6004) is used to buffer and condition the analog signal from the motor feedback before it is read by the microcontroller’s ADC input. The Curiosity Nano processes these analog readings and generates PWM control signals through its DAC and digital I/O pins to drive the H-Bridge.

The J2 connector provides external access to the system’s digital, analog, and ground pins for motor control and sensor interfacing. Overall, the design integrates signal processing, control, and actuation into a compact and efficient embedded motor control solution.
To get some initial formatting help, one can view ["here"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/Appendix/basic-markdown-examples/) some basic techniques.


##  Block Diagram 


<img width="680" height="558" alt="Image" src="https://github.com/user-attachments/assets/368d2f8e-b641-40c7-9ca5-02f3477d16d7" />
