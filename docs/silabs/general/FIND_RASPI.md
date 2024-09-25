# How to find your Raspberry Pi on the Network

## Finding the IP address of your Raspberry Pi

Sometimes it can be difficult to find your Raspberry Pi on the network. One way of interacting with the Raspberry Pi is to connect a keyboard, mouse, and monitor to it. The preferred method, however, is over SSH. For this, you will need to know the IP address of your Raspberry Pi.

This is a [good tutorial](https://raspberryexpert.com/find-raspberry-pi-ip-address/) on how to find the IP address.

### Mac / Linux

***Nmap***

The use of nmap on the Mac may require a software download.
Use nmap with the following command:

```shell
    $ sudo nmap -sn <subnet>.0/24`
```

Example: `sudo nmap -sn 10.4.148.0/24`, Among other returned values, you will see something: 

```shell
   $ Nmap scan report for ubuntu.silabs.com (10.4.148.44)
   $ Host is up (0.00025s latency).
   $ MAC Address: AA:BB:CC:11:22:33 (Raspberry Pi Trading)
```