## Overview

This firmware runs on the Microchip PIC18F57Q43 microcontroller and is responsible for generating, controlling, and managing the audio output and user interface functions of the system. The code configures all required peripherals including the DAC, PWM module, GPIO pins, and internal timers to ensure proper signal generation and timing control.

The DAC (RD5) is used to output the digital audio waveform as an analog signal, which is then sent to the external transistor amplifier and speaker. The PWM1 module (RB3) is configured to drive a status LED, providing real-time visual feedback of system activity. Internal timers regulate the sample rate and overall timing for consistent audio playback.

Digital I/O pins RD1, RD2, and RD6 are configured for general-purpose input/output, allowing for future expansion and testing. A push-button input is monitored by the firmware for user control functions such as triggering sounds or changing modes. All unused pins are properly initialized to avoid floating inputs and unintended behavior.

The firmware is written using Microchip MPLAB X and XC8, following a modular structure with clearly separated initialization, main execution loop, and interrupt service routines. This design allows for easy modification, debugging, and future feature expansion.

# example

<img width="783" height="783" alt="Image" src="https://github.com/user-attachments/assets/d73e3479-aeb3-4095-9423-29af18239f83" />

thats the [SpeakerFinal.zip](https://github.com/user-attachments/files/23918689/SpeakerFinal.zip)
