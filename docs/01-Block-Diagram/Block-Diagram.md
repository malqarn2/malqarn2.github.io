---
title: Individal Block Diagram
---

## Overview
This system uses a Microchip PIC18F57Q43 Curiosity Nano to generate audio signals that drive a speaker (FD3057) through a transistor amplifier. Power is supplied from a 9 V wall adapter, regulated to 5 V by an LM7805 voltage regulator.

The DAC1 (RD5) pin outputs the analog audio signal to the amplifier, which boosts the signal before sending it to the speaker. The PWM1 (RD7) pin drives a red LED for visual indication.

Additional digital I/O pins (RA3, RA4, RD6) are available for testing or controlling other devices. A test button is connected for user input.
An 8-pin connector provides access to analog, digital, and ground lines for external connections.

To get some initial formatting help, one can view ["here"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/Appendix/basic-markdown-examples/) some basic techniques.


##  Block Diagram 


<img width="741" height="756" alt="Image" src="https://github.com/user-attachments/assets/2a09b6c2-ea61-4ab7-9613-e381f5a8adce" />
