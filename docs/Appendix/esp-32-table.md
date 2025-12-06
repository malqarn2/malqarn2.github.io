---
title: Appendix – Example Controller Table for the PIC18F57Q43
---

| PIC Info | Answer | Help |
|---------|--------|------|
| Model | PIC18F57Q43 | Full Microchip part number |
| Product Page URL | [Microchip PIC18F57Q43 Product Page](https://www.microchip.com/en-us/product/PIC18F57Q43) | Found on Microchip.com |
| PIC18F57Q43 Datasheet URL | [PIC18F57Q43 Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F57Q43-Family-Data-Sheet-DS40002147.pdf) | Do not paste links directly, use a link |
| Technical Reference Manual URL | [PIC18F57Q43 Reference Manual](https://ww1.microchip.com/downloads/en/DeviceDoc/40002147E.pdf) | Has details on I/O, peripherals, etc |
| Vendor Link | [DigiKey PIC18F57Q43](https://www.digikey.com/) | DigiKey, Jameco, etc |
| Code Examples | [Microchip MCC Examples](https://www.microchip.com/en-us/tools-resources/configure/mplab-code-configurator) | Library and firmware examples |
| External Resources URL(s) | [YouTube PIC18F57Q43 Tutorials](https://www.youtube.com) | Search Google or YouTube |
| Unit Cost | ~$12.00 | Found on DigiKey |
| Absolute Maximum Current for entire IC | 200 mA | Found in datasheet |
| Supply Voltage Range | Min: 1.8V, Nominal: 5V, Max: 5.5V, Absolute Max: 6.0V | From datasheet |
| Maximum GPIO current (per pin) | 25 mA | From datasheet |
| Supports External Interrupts? | Yes | INT0 and pin-change interrupts |
| Required Programming Hardware, Cost, URL | MPLAB SNAP ($35) or Curiosity Nano (onboard debugger) | Microchip programmer |


| Module | # Available | Needed | Associated Pins (or * for any) |
|--------|-------------|--------|--------------------------------|
| UART | 2 | 1 | RC6 (TX), RC7 (RX) |
| external SPI* | 2 | 0 | * |
| I2C | 1 | 0 | * |
| GPIO | 49 | 5 | RD1, RD2, RB3, RA0, RA1 |
| ADC | 1 (12-bit) | 1 | RA1 |
| LED PWM | 5 | 1 | RB3 |
| Motor PWM | 5 | 0 | * |
| USB Programmer | 1 | 1 | Curiosity Nano onboard |
| DAC | 2 | 1 | RA0 |


\* The ESP32-S2 has multiple SPI interfaces, but some are for internal use
