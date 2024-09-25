# ZCL Advanced Platform (ZAP) Tool for Matter

## Overview

EFR32 example applications provide a baseline demonstration of a lock device,
built using the Matter SDK and the Silicon Labs GeckoSDK. It can be controlled
by a CHIP controller over OpenThread network.

The EFR32 device can be commissioned over Bluetooth Low Energy (BLE) where the
device and the CHIP controller will exchange security information with the
Rendez-vous procedure. Thread Network credentials are provided to the EFR32
device which will then join the network.

The LCD on the Silicon Labs WSTK shows a QR Code containing the needed
commissioning information for the BLE connection and starting the Rendez-vous
procedure.

The lock example is intended to serve both as a means to explore the workings of
CHIP, and a template for creating real products on the Silicon Labs platform.

Each Matter application consists of the following layers:


## Clusters

Every Matter Application uses multiple clusters leveraged from the Zigbee
Cluster Library (ZCL). A cluster can be seen as a building block for the Data
Model of a Matter application. Clusters contains attributes, commands, and
events. Attributes are customizable variables specified by the Zigbee Advanced
Platform (ZAP) tool. Commands are sent to the application, which may respond with
data, LED flickering, lock actuation, etc. Events are notifications sent out by
the server.

An application can have multiple Matter endpoints. Application endpoints
generally refer to one device, and inherits its information from the "cluster"
it belongs to. Utility clusters are required to be on the endpoint with ID 0.
Application clusters are assigned to endpoints with IDs 1 and higher.

Some applications have callbacks that are left to be implemented by the device
manufacturer. For example, the storage and management of users and credentials in
the lock-app is left up to the application developer.

## ZAP Tool

The ZAP tool is built and maintained by Silicon Labs and developers in the ZAP
open source community. It inherits its name and features from the Zigbee Cluster
Library, which was the starting point for the Matter data model. ZAP is used for
generating code for Matter applications based on the Zigbee Cluster Library and
associated Matter code templates.

The ZAP tool is no longer present as a submodule in the Matter repo. The ZAP tool 
can be downloaded as a binary from GitHub or optionally you can clone the entire ZAP 
repo and build the ZAP binary from scratch.

ZAP binaries can be downloaded from the latest ZAP release here:
