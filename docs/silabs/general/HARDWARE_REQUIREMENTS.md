# Matter Hardware Requirements

To run Matter over Thread or over Wi-Fi requires some Silicon Labs hardware in
order to run demos and do development. Following are the hardware requirements
for both Thread and Wi-Fi use cases broken down by platform and transport
protocol.

The following sections describe the hardware that may be used for Matter+OpenThread (Matter Hub and Accessory Device) and for Matter+Wi-Fi (Accessory Device). The EFRMG24 is the preferred starting point for Matter MCUs (including the Matter Hub RCP and both Accessory Devices). It provides Secure Vault and can use the internal flash of the device to store an upgrade image.

## Matter Over Thread "Matter Hub" Requirements

If you are running Matter over Thread and do not have a platform on which to run
the Open Thread Border Router and chip-tool, Silicon Labs recommends that you run
them on a Raspberry Pi. To do so you will need:

