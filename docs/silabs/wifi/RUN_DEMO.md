# Getting Started with EFR32 Host in NCP Mode
This page describes how to get started with developing an application on EFR32 host in Network Co-Processor (NCP) mode, where the application runs on the EFR32 host and the connectivity stack runs on the Wi-Fi chipset.

## Hardware Requirements
The following hardware devices are required for executing Matter over Wi-Fi for NCP Mode:
 - Additional hardwares required for NCP Boards:
## Software Requirements
Below are the software tools, packages and images required for executing Matter over Wi-Fi for NCP Mode:

### Software Tools Requirements
 - Simplicity Commander for flashing bootloader and binary on EFR32 Boards
 - Tera Term for flashing firmware on EFR32 NCP Boards.
 - Putty for controlling EFR32 hardware using chip-tool controller
 - Ozone Debugger for logging and debugging (Optional)
 - JLink RTT for logging only (Optional)

## Connect the Boards to a Computer
1. Mount the EFx32 radio board on the EFx32 WSTK board.
        
   ![Silicon Labs - design](./images/mount-efr32.png)

2. Connect the NCP expansion board to the EXP header on the EFx32 WSTK board.
        
   ![Silicon Labs - design](./images/mount-expansion.png)

3. Toggle the upper switch on the NCP expansion board to EXP-UART.

## Updating NCP Boards Connectivity Firmware