# GNS3-CISCO-Routers-Network-Examples
This repository contains examples of network configurations using CISCO router images in GNS3, along with two tested network topologies and a guide for properly configuring the TAP interface.

## Configure tap0 Interface

To configure the tap0 interface, follow these steps:

1. Open a terminal and run the following command to create the tap0 interface, replacing "username" with your actual username:

    ```
    tunctl -t tap0 -u username
    ```

2. Bring up the tap0 interface by executing the following command:

    ```
    ip link set tap0 up
    ```

3. Assign the IP address 10.0.0.3/8 to the tap0 interface using the following command:

    ```
    ip addr add 10.0.0.3/8 dev tap0
    ```

## Enable SNMP on a Router

To enable SNMP on a CISCO router, perform the following steps:

1. Access the router's configuration interface.

2. Set the read-only SNMP community string by entering the following command, replacing "rocom" with your desired community string:

    ```
    snmp-server community rocom RO
    ```

