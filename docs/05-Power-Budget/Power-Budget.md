---
title: Power Budget
---

## Overview
In this section, I created a Power Budget to calculate and analyze the total current and power requirements of the updated Speaker System circuit. The goal was to ensure that every component — including the Curiosity Nano microcontroller, push-pull amplifier (2N3904 and 2N3906), FD3057 speaker, and 5 V voltage regulator (LM7805) — operates safely within the available 9 V input power supply limits.

By estimating the current draw of each device and grouping them by voltage rail (9 V and 5 V), I verified that the selected 9 V adapter and LM7805 regulator can provide sufficient current for all components with an appropriate safety margin. This revised Power Budget replaces the previous motor-control configuration and reflects the new audio-output subsystem driven through a simple transistor amplifier.

Creating this Power Budget helps ensure reliable operation, preventing voltage sag, thermal overload on the LM7805, and unstable audio performance in the final design.



<img width="1146" height="817" alt="Image" src="https://github.com/user-attachments/assets/2331ec2e-9c38-4747-befe-21d06a575350" />
<img width="1221" height="468" alt="Image" src="https://github.com/user-attachments/assets/c04b6928-02e9-4a92-95d6-eadd4df15747" />{style width:"350" height:"300;"}



## Conclusions

From the prepared Power Budget, it was confirmed that the Speaker System circuit can safely operate within the limits of the 9 V power adapter and the 5 V LM7805 regulator.
The total current drawn by all components — including the Curiosity Nano, push-pull amplifier, and FD3057 speaker — remains well below the available supply capacity with an added 25 % safety margin.
Overall, the Power Budget validates that this updated speaker-based design is electrically sound, thermally safe, and well-suited for the AutoCan system’s audio-output requirements.

## Resouces

The power budget as a PDF download is available [*here*][Power_Budget_Speaker.pdf](https://github.com/user-attachments/files/23348479/Power_Budget_Speaker.pdf), and a Microsoft Excel Sheet [*here*][Power_Budget_Speaker.xlsx](https://github.com/user-attachments/files/23348486/Power_Budget_Speaker.xlsx).
