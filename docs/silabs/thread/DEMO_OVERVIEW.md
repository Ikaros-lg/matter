# Matter over Thread Demo Overview

This section reviews the steps for running an example lighting app for Matter
Thread setup.

At a high level, this section walks through starting a Thread network, commissioning a
new device to the Thread network using Bluetooth LE, and finally sending a basic
OnOff command to the end device.

## Step 0: Prerequisites

Before beginning your Silicon Labs Matter over Thread project be sure you have satisfied all

## Step 1: Setting up the Matter Hub (Raspberry Pi)

The Matter Hub consists of the Open Thread Border Router (OTBR) and the chip-tool running on a Raspberry Pi.
Silicon Labs has developed a Raspberry Pi image combining the OTBR and chip-tool that can be downloaded and
flashed onto an SD Card, which is then inserted into the Raspberry Pi.

The Matter Controller sends IPv6 packets to the OTBR, which converts the IPv6
packets into Thread packets. The Thread packets are then routed to the Silicon
Labs end device.

## Step 2: Flash the RCP

The Radio Co-Processor (RCP) is a Thread device that connects to the Raspberry
Pi via USB. To flash the RCP, connect it to your laptop via USB. Thereafter, it
should be connected to the Raspberry Pi via USB as well. Prebuilt RCP images are
available for the demo

