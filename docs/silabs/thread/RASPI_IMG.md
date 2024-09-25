# Setting up the Matter Hub (Raspberry Pi)

The Matter Hub consists of the Open Thread Border Router (OTBR) and the chip-tool
running on a Raspberry Pi. Silicon Labs has developed a Raspberry Pi image that
can be downloaded and flashed onto an SD Card for the Raspberry Pi.

In short, the Matter Controller sends IPv6 packets to the OTBR, which converts
the IPv6 packets into Thread packets. The Thread packets are then routed to the
Silicon Labs end device.

## How to use the Silicon Labs Matter Raspberry Pi Image (Matter Hub)


### Step 1. Raspberry Pi Image Download

The provided Raspberry Pi image is used as a Matter Controller with the OTBR.

The image can be downloaded from the

### Step 2. Flashing your Raspberry Pi

[Raspberry Pi Disk Imager](https://www.raspberrypi.com/software/) can be used to
flash the SD Card that contains the operating system for the Raspberry Pi. Under
Operating System select 'Use Custom' and then select the .img file.

Alternatively, a tool like [balenaEtcher](https://www.balena.io/etcher/) can be
used to flash the image to a micro SD card.
