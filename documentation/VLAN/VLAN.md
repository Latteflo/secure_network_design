# VLAN documentation 

When it comes to networking, VLANs are the unsung heroes. They’re like the secret agents of the network world, keeping things running smoothly behind the scenes.

In our project we decided to use VLANs to divide our network into smaller, more manageable chunks. This way, we can keep our network traffic organized and secure.

## VLANs in Our Network
 - Each VLAN has its own subnet, and we've got a plan for every IP.
        Here's the breakdown:
      - **VLAN 10:** The Servers. Where the internet meets the network.
      - **VLAN 20:** The cool kids' table. Management and Support.
      - **VLAN 30:** Where Study get stuff done.
      - **VLAN 40:** Production's playground.

## IP Addressing Scheme

This section details the IP addressing layout designed for the secure network. Each sector of the network is allocated a specific IP range and VLAN ID to segregate traffic efficiently and enhance security.

We also have a subnetting strategy in place to ensure that each sector has adequate IP addresses for current and future needs.


| Sector           | IP Range          | Subnet Mask     | VLAN ID | Usable Hosts |
|------------------|-------------------|-----------------|---------|--------------|
| Management       | `192.168.10.0/24` | `255.255.255.0` | `10`    | 254          |
| Study            | `192.168.20.0/24` | `255.255.255.0` | `20`    | 254          |
| Production       | `192.168.30.0/24` | `255.255.255.0` | `30`    | 254          |
| Support Sector 1 | `192.168.40.0/24` | `255.255.255.0` | `40`    | 254          |
| Support Sector 2 | `192.168.50.0/24` | `255.255.255.0` | `50`    | 254          |

### Subnetting Strategy

The IP addressing scheme utilizes a subnetting strategy that allows for efficient use of IP space while ensuring each sector has adequate addresses for current and future needs. Each subnet is designed to accommodate the specific number of workstations and devices in its sector, with room for expansion.

Addresses within each subnet are allocated as follows:

- The first usable IP (`x.x.x.1`) is typically assigned to the gateway/router interface that serves each subnet.
- Static IPs (`x.x.x.2` to `x.x.x.10`) are reserved for servers, printers, and other permanent devices.
- DHCP is configured to dynamically assign IPs starting from `x.x.x.11` onwards to workstations and temporary devices.

This systematic approach to IP allocation simplifies network management, aids in troubleshooting, and enhances security through clear segmentation.
