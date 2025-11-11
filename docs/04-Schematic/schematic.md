---
title: Schematic
---

## Overview

Overview

Overview
This schematic powers a Curiosity Nano board and drives a speaker. It includes a 9 V to 5 V voltage regulator, a small audio amplifier, and connection headers for I/O.

Power Supply
A 9 V input is regulated to 5 V using an LM7805. The 5 V output powers the Curiosity Nano, the amplifier circuit, and other components. Capacitors smooth the voltage and reduce noise.

Controller (Curiosity Nano)
The Curiosity Nano microcontroller provides the control or audio signal (V_in) and manages overall operation. A 0.1 µF capacitor filters its power line for stability.

Speaker Amplifier
Two 2N3904 transistors form a simple push-pull amplifier to drive a speaker.
Diodes 1N4148 bias the transistors, while resistors set the input and base currents.
A 10 µF capacitor couples the signal to the speaker and blocks DC.

Connectors

J1: Barrel jack for 9 V input.

J2: 8-pin header for Curiosity Nano I/O connections.

Ground
All sections share a common ground to ensure reliable and stable operation.

<img width="1712" height="790" alt="Image" src="https://github.com/user-attachments/assets/eed52cfb-1717-4fac-878f-fdbcdc18a444" />
**Figure 1:** Showing a schematic.


## Resouces

The schematic as a PDF download is available [*here*][Speaker_schematic.pdf](https://github.com/user-attachments/files/23409316/Speaker_schematic.pdf), and the Zip folder of the project [*here*][Speaker_schematic.zip](https://github.com/user-attachments/files/23409460/Speaker_schematic.zip).
