# Unify Matter Protocol Controller User Guide

The Unify Matter PC is a Unify Protocol Controller that enables interaction between
Unify network and a Matter fabric. For a more thorough description see the

This guide assumes that you have set up
Unify SDK. Read the
[Unify Host SDK's Getting Started Guide](https://siliconlabs.github.io/UnifySDK/doc/getting_started.html)
for information on how to set this up.

Once a Unify SDK is setup, the Matter PC can be started.

The following documentation assumes that you have built the Unify Matter PC
transferred the _`unify-matter-pc`_ to your Raspberry Pi 4 (RPi4) running
the 64-bit version of Raspberry Pi OS Bullseye.


## Running the Matter PC

At start-up, the Matter PC needs to connect to the Matter Fabric as well as
the MQTT Broker. It is therefore critical that you have access to port 1883, the
default MQTT Broker's port, as well as a network setup that allows mDNS through.

A few important runtime configurations must be considered, along with some other
configuration options. A full list of command-line parameters is provided in the
[Command line arguments](#command-line-arguments) section.

### Important Configuration Settings
