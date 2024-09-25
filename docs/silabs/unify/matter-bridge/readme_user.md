# Unify Matter Bridge User Guide

The Unify Matter Bridge is a Unify IoT Service that enables interaction with
Unify devices from a Matter fabric. For a more thorough description see the

As a prerequisite for the Matter Bridge to work, at least one Unify protocol
controller should be set up and running. This guide assumes that you have set up
the Z-Wave Protocol Controller (uic-zpc) to run on a Raspberry Pi 4 and
connected it to an MQTT broker in your network. Read the
[Unify Host SDK's Getting Started Guide](https://siliconlabs.github.io/UnifySDK/doc/getting_started.html)
for information on how to set this up.

Once a protocol controller is running, the Matter Bridge can be started.

The following documentation assumes that you have built the Unify Matter Bridge
transferred the _`unify-matter-bridge`_ to your Raspberry Pi 4 (RPi4) running
the 64-bit version of Raspberry Pi OS Bullseye.

## Running the Matter Bridge

At start-up, the Matter Bridge needs to connect to the Matter Fabric as well as
the MQTT Broker. It is therefore critical that you have access to port 1883, the
default MQTT Broker's port, as well as a network setup that allows mDNS through.

A few important runtime configurations must be considered, along with some other
configuration options. A full list of command-line parameters is provided in the
[Command line arguments](#command-line-arguments) section.

### Important Configuration Settings

