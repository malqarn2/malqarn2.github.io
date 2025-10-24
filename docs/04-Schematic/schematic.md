---
title: Schematic
---

## Overview

Overview

This schematic provides regulated power and signal connections for a Curiosity Nano microcontroller board. It includes a 5 V voltage regulator, an op-amp circuit for analog signal buffering, and a connector for external inputs and outputs.

Power:
A 9 V input is regulated to 5 V using the LM7805 voltage regulator. The regulated 5 V output supplies power to the Curiosity Nano board, the LM324 op-amp, and other circuit components.

Op-Amp (LM324):
The LM324 is configured as a voltage follower to buffer and stabilize the analog signal from a sensor before it is read by the Nano’s analog input pin.

Controller (Curiosity Nano):
The Curiosity Nano microcontroller processes the buffered analog signal and manages input/output operations through connector J2.

Connector (J2):
An 8-pin header provides access to the Nano’s I/O pins for additional sensors, modules, or external connections.

Ground:
All components share a common ground reference to maintain stable and reliable operation throughout the circuit.

<img width="1645" height="860" alt="Image" src="https://github.com/user-attachments/assets/d8b2e5fa-f48f-4d26-aa45-2045cf217195" />
**Figure 1:** Showing a schematic.


## Resouces

The schematic as a PDF download is available [*here*][subsystem schematic PDF.pdf](https://github.com/user-attachments/files/23130336/subsystem.schematic.PDF.pdf), and the Zip folder of the project [*here*][schematic.Zip.zip](https://github.com/user-attachments/files/23012312/schematic.Zip.zip).
