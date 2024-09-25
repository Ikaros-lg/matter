# Creating Gecko Bootloader for Use in Matter OTA Software Update

The Matter OTA Software Update functionality on EFR32 devices requires the use
of a Gecko Bootloader built with correct configuration parameters. The key
parameters are the storage slot size and (in case of internal storage) storage
slot address. The current document lists the steps required to build the Gecko
Bootloader for Matter OTA Update and discusses the configuration parameter
selection. For a detailed discussion of Gecko Bootloader refer to _UG489:
Silicon Labs Gecko Bootloader User's Guide for GSDK 4.0 and Higher_.

The Gecko Bootloader is built with Silicon Labs Simplicity Studio. These
instructions assume that you have installed Simplicity Studio 5, the Simplicity
Commander tool (installed by default with Simplicity Studio), the GSDK and
associated utilities, and that you are familiar with generating, compiling, and
flashing an example application in the relevant version.

## Bootloader Project In Studio

### Creating the Project

In Simplicity Studio click on Project->New->Silicon Labs Project Wizard to
create a new project. Select the correct Target Board, SDK and the Toolchain.
For Matter 1.0 it is recommended that the bootloader is built with GSDK 4.1.

In the next screen select the example project the bootloader will be based on.
For a bootloader using external storage select "Bootloader SoC SPI Flash Storage
(single image with slot size of 1024K)". For a bootloader using internal storage
select "Bootloader - SoC Internal Storage (single image on 512kB device)"

### Configuring Storage Components and Parameters

In the newly created project select the project's .slcp file, click the
"Software Components" tab, and select Platform->Bootloader->Storage. In the
Bootloader Storage Slot component (it should be already installed) configure
Slot 0's Start Address and Slot size.

### Configuring Other Components

It is recommended to install the "GBL Compression (LZMA)" component under
Platform->Bootloader->Core: this allows the bootloader to handle compressed GBL
files. This component is required for internal storage bootloaders.

At this point the project contains all the components necessary to support the
Matter OTA Software Update functionality. Other components can now be added to
support additional features such as Secure Boot. Refer to _UG489: Silicon Labs
Gecko Bootloader User's Guide for GSDK 4.0 and Higher_ for the description of
various Bootloader features and the steps to enable them.

### Building and Flashing the Bootloader

Build the project by clicking on the hammer icon in the Studio toolbar. Flash
the bootloader to the board using the "Upload Application" option from the Debug
Adapters view.

### Combined bootloader for MG12 boards

The MG12 boards (which are Series 1 EFR32 boards) require a combined bootloader
image (first stage bootloader + main bootloader) the first time a device is
programmed -- whether during development or manufacturing. For subsequent
programming, if the combined bootloader had been previously flashed to the
device use the regular version.

To create the combined bootloader follow this additional step (Step 6 in Section
6 of _UG489: Silicon Labs Gecko Bootloader User's Guide for GSDK 4.0 and
Higher_) before clicking the build icon: Right-click the project name in the
Project Explorer view and select Properties. In the C/C++ Build group, click
Settings. On the Build Steps tab, in the Post Build Steps Command field enter

```shell
$ ../postbuild.sh "${ProjDirPath}" "${StudioSdkPath}" "${CommanderAdapterPackPath}"
```

## Internal Bootloader: Image Size, Selecting Storage Slot Address and Size

The internal storage bootloader for Matter OTA software update is supported on
MG24 boards only. In this use case both the running image and the downloadable
update image must fit on the internal flash at the same time. This in turn
requires that both images are built with a reduced feature set such as disabled
