---
title: Welcome
tags:
- tag1
- tag2
---
<center>
<font size= "6">Mohammed Ali Datasheet</font><br>
as part of<br>
<font size= "8"> Auto Can </font><br>
for<br>
<font size= "5"> Team 202 </font><br>

**Submission: 10, 26, 2025**
</center>

## Introduction

* The purpose of this datasheet is to provide a detailed overview of the Smart Trash project, including its components, Block Diagram, and functionality. This document serves as a technical reference for understanding how each subsystem, electrical, and software works together to achieve automated Speaker integration.
### Project Summary

* The part I’m working on is the Speaker Subsystem, which is responsible for generating audio output for the AutoCan system. This subsystem uses a push-pull amplifier circuit built with 2N3904 (NPN) and 2N3906 (PNP) transistors to drive the FD3057 speaker. The amplifier receives its input from the Curiosity Nano’s DAC1 output, which produces analog signals such as tones or alerts.

The amplified signal is then sent through a coupling capacitor to the speaker, allowing the system to play sound notifications—for example, to indicate when the bin is opening or closing. Powered by a 5 V regulator (LM7805) from a 9 V barrel supply, the circuit provides clean and reliable audio output.

This subsystem enhances user interaction by adding audible feedback, improving accessibility and awareness during system operation.
* Add context that ties into the link to your [team report.](https://egr304-2025-f-202.github.io/)

### My Contribution

* My specific contribution focused on the Speaker Subsystem, which is responsible for generating audio feedback within the AutoCan system. I designed and implemented a push-pull transistor amplifier using 2N3904 (NPN) and 2N3906 (PNP) transistors to drive the FD3057 speaker. The circuit receives an analog audio signal from the Curiosity Nano’s DAC output, amplifies it, and outputs a clear tone through the speaker.
  
To review the details listed of the material used to construct the subsection, you can review it in the ["BOM"](https://embedded-systems-design.github.io/EGR304DataSheetTemplate/03-BOM/BOM/) section of the datasheet.

For all the sections
