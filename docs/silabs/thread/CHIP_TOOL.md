# Using the Matter Hub and the Mattertool (chip-tool)

The following commands show how to start a new Thread network from the local
OTBR, commission an EFR32 Matter End Device (Matter Accessory Device), and then
send the on/off commands with the `mattertool` automated script. The `mattertool` 
script provides an interface into various chip-tool and otbr commands used to create 
and interact with a Matter network

## Basic Mattertool Commands

| **Command**              | **Usage**                                                                 |
| ------------------------ | ------------------------------------------------------------------------- |
| `mattertool startThread` | Starts the thread network on the OTBR                                     |
| `mattertool bleThread`   | Starts commissioning of a Matter Accessory Device using the chip-tool      |
| `mattertool on`          | Sends the _on_ command to the Matter Accessory Device using the chip-tool  |
| `mattertool off`         | Sends the _off_ command to the Matter Accessory Device using the chip-tool |

You can also use the full chip-tool command set (still using mattertool)

```shell
$ mattertool levelcontrol read current-level 106 1
```

## Advanced Information on the Matter Hub

### Image tree

## Open Thread Border Router (OTBR)

For information on what commits to use for the OTBR and RCP, consult the

The pre-installed OTBR is configured for the infrastructure interface eth0.

Bash script to modify, reinstall or update the OTBR:

```shell
$ otbrsetup
```

This bash script centralizes and simplifies the local OTBR installation.

Available commands:

| **Command**                    | **Description**                                                                                                                    |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| -h, --help                     | Prints help options                                                                                                                |
| -if, --interface <eth0\|wlan0> | Select infrastructure interface. Default eth0                                                                                      |
| -i, --install                  | Bootstrap, set up and install the OTBR. Usually for a new installation                                                             |
| -s, --setup                    | Runs the OTBR setup only, use this to change the configured infrastructure interface (use in combination with -if wlan0 for Wi-Fi) |
| -u, --update                   | Update the OTBR installation after the repo is updated                                                                             |
