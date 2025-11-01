---
title: Power Budget
---

## Overview
In this section, I created a Power Budget to calculate and analyze the total current and power requirements of the AutoCan system. The goal was to ensure that every component in the circuit including the Curiosity Nano microcontroller, op-amp, voltage regulator, H-Bridge, and DC motor operates safely within the available power supply limits.

By estimating the current draw of each device and grouping them by voltage rail (9 V and 5 V), I was able to confirm that the selected 9 V power adapter and 5 V regulator can provide sufficient current with an appropriate safety margin. Creating this Power Budget helps prevent power shortages, overheating, and unstable operation in the final circuit design.



<img width="1413" height="763" alt="Image" src="https://github.com/user-attachments/assets/ee27392d-322a-4ff4-b900-b5802d43ec66" />
<img width="1393" height="712" alt="Image" src="https://github.com/user-attachments/assets/2d2d029f-1f79-437d-bd33-8cbd562ad094" />{style width:"350" height:"300;"}



## Conclusions

From the prepared Power Budget, it was confirmed that the AutoCan circuit can safely operate within the limits of the selected 9 V power adapter and 5 V voltage regulator. The total current drawn by all components, including the Curiosity Nano, LM324 op-amp, H-Bridge, and DC motor, remains below the available supply capacity with an added 25% safety margin. This ensures stable operation, prevents voltage drops, and avoids overloading the power supply. Overall, the Power Budget validates that the design is electrically reliable and suitable for the AutoCan system’s requirements.

## Resouces

The power budget as a PDF download is available [*here*][Power Budget.pdf](https://github.com/user-attachments/files/23202884/Power.Budget.pdf), and a Microsoft Excel Sheet [*here*][Power_Budget_Mo.xlsx](https://github.com/user-attachments/files/23202891/Power_Budget_Mo.xlsx).
