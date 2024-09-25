# Silicon Labs Matter New Features

## New Features for v2.3.0-1.3

- Matter 1.3 solution for Thread (MG12, MG24), Wi-Fi NCP platforms (MG24/RS9116, MG24/WF200, MG24/SiWx917) and Wi-Fi SoC platform (SiWx917).
  - Long Idle Time ICDs are ready for integration.
  - Provides Multi-chip OTA functionality support (EFR32-Thread only).
  - Adds Provisioning 2.0 Support for EFR32 and SiWx917 SoC.
  - Stability and sleep improvements for SiWx917 SoC have been added for both the TA and M4.
  - Enables LCD and OTA support (M4 image only) for MG24+SiWx917 NCP.
- Miscellaneous bug fixes and improvements

## New Features for v2.3.0-1.3-alpha.2

- Enhanced 917 SoC sleep functionality
  - Sleepy OTA upgrade functionality
  - M4 sleep optimization while device is uncommissioned
  - M4 sleep optimization when commissioning retry sequence experiences ongoing delay
  - Clock usage: Makes use of default sleep clock vs. high frequency clock

## New Features for v2.3.0-1.3-alpha.1

- Update to use [Gecko SDK (GSDK) v4.4.0](https://docs.silabs.com/gecko-platform/4.4.0/platform-overview/)
- Update to use [WiSeConnect 3 SDK (WiFi SDK) v3.1.1](https://docs.silabs.com/wiseconnect/3.1.1/wiseconnect-developing-with-wiseconnect-sdk/)
- Matter 1.3 alpha support
- Matter ICD Long Idle Time (LIT) provisional support
  - **Note**: Controllers do not fully support at time of release
- 917 SoC OTA Upgrade
- 917 SoC Custom Part Manufacturing Service (CPMS) Feature

## New Features for v2.2.0-1.2

- GA support for Intermittently Connected Devices
- Introduction of a third LCD screen to display application information
- Introduction of the Dishwasher Demo Application
- Adds support of Matter 1.2 Apps on all Wi-Fi devices.
- Adds Matter support on SiWx917 SoC Common flash variants - BRD4338A.
- Adds LCD display support on SiWx917 SoC for all the Wi-Fi Matter Apps.
- Adds support for Direct Internet Connectivity on the SiWx917 SoC & NCP

### ICD Sample Apps
With the official introduction of Matter Short Idle Time (SIT) ICDs, both the door-lock sample app and the light-switch sample app are configured as SIT ICDs by default.
The default configurations can be found in their respective openthread.gni.

### Self-Provisioning Mode

Silicon Labs' Matter examples now include a self-provision mode, which enables the application to be used as Generator Firmware with the provisioning script:

To enter the self-provisioning mode, factory reset the device pressing buttons BTN0 and BTN1 for six seconds. Using this method, the device application only needs to be flashed once, provisioned multiple times, and be ready for commissioning after each provisioning.

## New Features for v2.2.0-1.2-alpha.1

### Support for Intermittently Connected Devices (ICD)