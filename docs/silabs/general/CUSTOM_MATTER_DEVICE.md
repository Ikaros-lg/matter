# Custom Matter Device Development

Build a customizable lighting app using the Matter protocol.

## Overview

This guide covers the basics of building a customizable lighting application
using Matter.

## Using Matter with Clusters

In Matter, commands can be issued by using a cluster. A cluster is a set of
attributes and commands which are grouped together under a relevant theme.

Attributes store values (think of them as variables). Commands are used to
modify the value of attributes.

For example, the "On/Off" cluster has an attribute named "OnOff" of type
boolean. The value of this attribute can be set to "1" by sending an "On"
command or it can be set to "0" by sending an "Off" command.

The C++ implementation of these clusters is located in the clusters directory.
Note that you can also create your own custom cluster.

## ZAP Configuration

From the matter repository, run the following command in a terminal to launch
the ZAP user interface (UI). This will open up the ZAP configuration for the EFR32 lighting
application example.

