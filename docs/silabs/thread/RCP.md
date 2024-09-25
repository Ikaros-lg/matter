# How to Build and Flash the Radio Co-Processor (RCP)

The Radio Co-Processor is a 15.4 stack image flashed onto a Silicon Labs
development kit or Thunderboard Sense 2. The 15.4 stack on the development kit
communicates with the higher layers of the Thread stack running on the Raspberry
Pi over a USB connection.

A complete list of supported hardware for the RCP is provided on the

First, in order to flash the RCP, connect it to your laptop directly by USB.

## Step 1: Get or Build the Image File to Flash the RCP

We have provided two ways to get the required image to flash the RCP. You can
use one of the following options:

1. Use the pre-built 'ot-rcp' image file
2. Build the image file from the 'ot-efr32' repository, which is listed on the

### **Using a Pre-built Image File**

RCP image files for all demo boards are accessible through the

### **Building the Image File from the ot-efr32 Repository**

**1. Clone the ot-efr32 repository**

The 'ot-efr32' repo is located in Github here:
https://github.com/SiliconLabs/ot-efr32.

You must have Git installed on your local machine. To clone the repo use the
following command:

```shell
$ git clone https://github.com/SiliconLabs/ot-efr32.git
```

Once you have cloned the repo, enter the repo and sync all the submodules with
the following command:

```shell
$ cd ot-efr32
```

```shell
$ git submodule update --init
```

After updating the submodules you can check out the correct branch or commit
hash for the system. Check the current branch and commit hash used here:

```shell
$ git checkout <commit hash>
```