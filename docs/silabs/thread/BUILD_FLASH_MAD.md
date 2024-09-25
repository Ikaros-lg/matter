# How to Build and Flash the Matter Accessory Device (MAD)

The Matter Accessory Device, such as the lighting-app, is the actual Matter
device that you will commission onto the Matter network and control using the
chip-tool.

## Step 1: Get the Image File to Flash the MAD

We have provided two ways to get the required image to flash the MAD. You can
use one of the following options:

1. Use the pre-built image file
2. Build the image file from the '`matter`' repository

-   ### **Building the Matter Image File from the Repository**

    The Matter Accessory Device (lighting-app) can be built out of this repo.

    Documentation on how to build and use the lighting-app Matter Accessory
    Device is provided in this

    Please note that you only need to build a single device for the demo such as
    the lighting-app. If you wish to build other examples such as the sleepy end
    device you are welcome to, but it is not necessary for the demo.

    or [/silabs_examples](https://github.com/SiliconLabs/matter/blob/latest/silabs_examples/) (such as `onoff-plug-app`).

    The build process puts all image files in the following location:


## Step 2: Flash the Matter Accessory Device

For more information on how to flash your Silabs development platform see the
following instructions:

Once your Matter Accessory Device has been flashed it should show a QR code on
the LCD. If no QR Code is present it may be that you need to add a bootloader to
your device. Bootloader images are provided on the
