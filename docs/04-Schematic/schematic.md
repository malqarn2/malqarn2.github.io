---
title: Schematic
---

## Overview

Overview

This schematic powers and controls a Curiosity Nano microcontroller board with a DC motor. It includes a 9 V to 5 V power regulator, an op-amp for analog signal buffering, and a discrete H-Bridge for motor control.

Power Supply

A 9 V input is regulated to 5 V using an LM7805. The 5 V output powers the Curiosity Nano, the LM324 op-amp, and other components. Capacitors help smooth voltage and reduce noise.

Op-Amp (LM324)

The LM324 buffers and stabilizes analog signals from sensors before they are read by the Curiosity Nano’s analog input.

Motor Driver (H-Bridge)

A discrete H-Bridge  drives the DC motor in both directions. The Curiosity Nano provides the control signals.

Controller (Curiosity Nano)

The Curiosity Nano reads sensor signals, sends control signals to the H-Bridge, and manages overall system operation.

Connector (J2)

An 8-pin header provides access to the Curiosity Nano’s I/O pins for connecting sensors, modules, or external devices.

Ground

All components share a common ground to ensure stable and reliable operation.

<img width="1181" height="817" alt="Image" src="https://github.com/user-attachments/assets/83a5c6d2-9d32-486c-bdbe-2abc8e117684" />
**Figure 1:** Showing a schematic.


## Resouces

The schematic as a PDF download is available [*here*][Schematic PDF.pdf](https://github.com/user-attachments/files/23200744/Schematic.PDF.pdf), and the Zip folder of the project [*here*][schematic.Zip.zip](https://github.com/user-attachments/files/23200748/schematic.Zip.zip).
