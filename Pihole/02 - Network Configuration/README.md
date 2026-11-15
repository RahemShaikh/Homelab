# 02 - Network Configuration

## Overview

Configure network connectivity for the Raspberry Pi and establish a consistent IP address through a DHCP reservation.

## Network Configuration

| Setting | Configuration |
|---|---|
| IP Address | `192.168.0.123` |
| Subnet Mask | `255.255.255.0` |
| IP Assignment | DHCP Reservation |
| DNS Servers (Prior to Pi-hole) | `68.105.28.11`, `68.105.29.11` |
| Connection | Ethernet |

## IP Reservation

After connecting the Raspberry Pi to the network through Ethernet, the router's DHCP server automatically assigned it an IP address.

I accessed the router's administration interface and created a DHCP reservation for the Raspberry Pi using its Ethernet MAC address. This ensures the device receives the same IP address whenever it reconnects to the network.

![DHCP Reservation](Images/router-dhcp-reservation.png)

## Verification

The following Linux commands were used to inspect and verify the network configuration:

| Command | Purpose |
|---|---|
| `hostname -I` | Display assigned IP address(es) |
| `ip route` | Display routing table and default gateway |
| `ifconfig` | Display network interface configuration |
| `cat /etc/resolv.conf` | Display configured DNS nameservers |

## What I Learned

- How to inspect network configuration using Linux terminal commands.
- How to configure a DHCP reservation through a router's administration interface.
- How to identify network interfaces and their assigned IP addresses.
- How to inspect DNS resolver configuration on Linux.