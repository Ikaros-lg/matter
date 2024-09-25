# Matter Wi-Fi Direct Internet Connectivity
-  Direct Internet Connectivity (DIC) is a silabs only feature to connect matter devices to proprietary cloud solutions(AWS,GCP,APPLE ...) directly.  As such, a Matter Wi-Fi device must support connecting locally on the Matter Fabric, via IPv6, and connecting to the Internet via IPv4.
-  Matter devices can be controlled by chip-tool or controller and the respective status of the attribute modified will be published to the cloud.
-  Remote user can install the cloud specific application to get the notification on the attribute status.

## DIC Feature Diagram
1. Below diagram gives end-to-end flow about Direct Internet Connectivity.
  
  ![Silicon Labs - DIC design](./images/dic-flow.png)

## Prerequisites

### Hardware Requirements

### Software Requirements
- [Download](https://github.com/thomasnordquist/MQTT-Explorer/releases/download/0.0.0-0.4.0-beta1/MQTT-Explorer-Setup-0.4.0-beta1.exe) MQTT Explorer Software for controlling device through cloud.

## End-to-End Set-up bring up
## Message Queuing Telemetry Transport (MQTT)

- MQTT is an OASIS standard messaging protocol for the Internet of Things (IoT). It is designed as an extremely lightweight publish/subscribe messaging transport that is ideal for connecting remote devices with a small code footprint and minimal network bandwidth. Refer https://mqtt.org/ for more details

### Configuration of MQTT server
