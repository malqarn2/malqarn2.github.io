---
title: Individal Block Diagram
---

## Overview
This system uses a Microchip PIC18F57Q43 Curiosity Nano to generate audio signals that drive a speaker (FD3057) through a transistor amplifier. Power is supplied from a 9 V wall adapter, regulated to 5 V by an LM7805 voltage regulator.

The DAC1 (RD5) pin outputs the analog audio signal to the amplifier, which boosts the signal before sending it to the speaker. The PWM1 (RB3) pin drives a red LED for visual indication.

Additional digital I/O pins (RD1, RD2, RD6) are available for testing or controlling other devices. A test button is connected for user input.
An 8-pin connector provides access to analog, digital, and ground lines for external connections.




##  Block Diagram 


<img width="751" height="756" alt="Image" src="https://github.com/user-attachments/assets/9f3333ec-02db-42ba-a6e2-d0b3a8d94f89" />
