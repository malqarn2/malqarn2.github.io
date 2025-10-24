---
title: Schematic
---

## Overview

Overview

This schematic provides power and signal connections for a Curiosity Nano microcontroller board. It includes a 5 V regulator, an op-amp for buffering a sensor signal, and a connector for inputs and outputs.

Power:
A 9 V input is regulated to 5 V by the LM7805. The 5 V output powers the Curiosity Nano, the op-amp, and other components.

Op-Amp (LM324):
Used as a voltage buffer to condition the sensor signal before it goes to the Nano’s analog input.

Controller:
The Curiosity Nano reads the buffered signal and handles digital I/O through connector J2.

Connector (J2):
Provides access to the Nano’s pins for external sensors or modules.

Ground:
All parts share a common ground for stable operation.
<img width="1645" height="860" alt="Image" src="https://github.com/user-attachments/assets/d8b2e5fa-f48f-4d26-aa45-2045cf217195" />
**Figure 1:** Showing a schematic.


## Resouces

The schematic as a PDF download is available [*here*][subsystem schematic PDF.pdf](https://github.com/user-attachments/files/23012193/subsystem.schematic.PDF.pdf), and the Zip folder of the project [*here*][schematic.Zip.zip](https://github.com/user-attachments/files/23012312/schematic.Zip.zip).
