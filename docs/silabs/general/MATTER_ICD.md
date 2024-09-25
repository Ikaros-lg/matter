# Matter Intermittently Connected Devices (ICD)

Matter introduces the concept of Intermittently Connected Devices (ICD) in the SDK and in the specification.
An Intermittently Connected Device is the Matter representation of a device that is not always reachable.
This covers battery-powered devices that disable their underlying hardware when in a low-power mode or devices that can be disconnected from the network, like a phone app.

This page focuses on features designed to improve the performance and reliability of battery-powered devices and their different configuration options.

## ICD Configurations

The ICD feature-set offers two types of configurations : cluster configurations and subscription configurations.
The cluster configurations are exposed through the ICD Manager Cluster interface.
The subscription configurations are exposed through build arguments and public APIs of the Matter SDK.

### ICD Management Cluster

The ICD Management Cluster enables configuration of the ICD’s behavior.
It is required for an ICD to have this cluster enabled on endpoint 0 to be certifiable.

#### Configuration Attributes

The ICD Management Cluster exposes three configuration attributes.
These configurations are independent from the underlying transport configurations.


```