# Building a Wi-Fi End Device for Matter in GitHub

## Software Setup

If you have not downloaded or cloned this repository, you can run the following
commands on a Linux terminal running on either Linux machine, WSL or Virtual
Machine to clone the repository and run bootstrap to prepare to build the sample
application images. Users may need to run the various commands as the root user or with certain privilges enabled.

1. To download the
   [SiliconLabs Matter codebase](https://github.com/SiliconLabs/matter.git) run
   the following commands.

    ```shell
     $ git clone https://github.com/SiliconLabs/matter.git
    ```

2. Bootstrapping:

    ```shell
    $ cd matter
    $ ./scripts/checkout_submodules.py --shallow --recursive --platform efr32
    $ . scripts/bootstrap.sh
    # Create a directory where binaries will be updated/compiled called `out`
    $ mkdir out
    ```
3. Troubleshooting the errors:
   
   1. For resolving [Git Submodule Error](./images/git_submodule_error.png), run below command:
      ```shell
      $ git submodule update --init --checkout
      ```
   2. For resolving [Bootstrapping Error](./images/Boostrapping_Error.png), run below command:
      ```shell
      $ pip install --upgrade prompt-toolkit
      ```
## Compiling the chip-tool

In order to control the Wi-Fi Matter Accessory Device you will have to compile
and run the chip-tool on either a Linux, Mac or Raspberry Pi. The chip-tool builds
faster on the Mac and Linux machines so that is recommended, but if you have
access to a Raspberry Pi that will work as well.

1. Build the chip-tool

    ```shell
    $ ./scripts/examples/gn_build_example.sh examples/chip-tool out/standalone
    ```

    This will build chip-tool in `out/standalone`.

## Using the Matter Accessory Device (MAD) Pre-Built Binaries

If you are just running the Matter demo, and are not interested in building the
Matter Accessory Device images from scratch, you can download the MAD images for
Wi-Fi from this software release on the