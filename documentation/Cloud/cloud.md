# Cloud - The Internet Simulation

Our network wouldn't be complete without the internet. We've got a Cloud-PT device to simulate the internet connection.

![alt text](internet.png)

Here's how we set it up:
### Cloud-PT Cloud2

Represents the Internet or an external network with an IP address of 0.0.0.0.

### Routers (1941)

Two Cisco 1941 routers are present:

- **IntermediateRouter0**: Connects to the Cloud2 and forwards traffic from the ISPdns area to IntermediateRouter1. Its external interface is marked with a red line indicating either down status or an issue with the connection, labeled with the IP `10.1.2.`

- **IntermediateRouter1**: Connects to IntermediateRouter0 and the ISPadministrator area, with an operational interface labeled with the IP `10.2.1.`

### ISP Routers (1941)

Two additional Cisco 1941 routers labeled as ISPdns and ISPadministrator, each connecting to different networks:

- **ISPdns**: Serves the DNS area with an IP address of `8.8.8` on its interface, simulating a public DNS server like Google DNS.

- **ISPadministrator**: Serves an administrative network area with an interface IP address of `150.1.1`.

### Switches (2960-24TT)

Two Cisco Catalyst 2960-24TT switches are involved in connecting the end devices to the respective routers.

- **Switch6**: Connected to the ISPdns router and the SBC-PT and Server-PT (GoogleDNS).

- **Switch5**: Connected to the ISPadministrator router and the PC-PT (PC3).

### End Devices

- **SBC-PT (SBC0)**: Likely a single-board computer or a server device, connected to the Switch6.
- **Server-PT (GoogleDNS)**: A server acting as a DNS server connected to Switch6.
- **Server-PT (Google)**: A web server connected to Switch5.
- **PC-PT (PC3)**: A client computer connected to Switch5.

## Network Segments and IP Addressing

- **DNS Segment**: Has a server acting as a DNS server with the iconic IP address of 8.8.8.8, simulating a public DNS service like Google's.
- **Web Server Segment**: Contains a web server simulating Internet service.
- **Client Segment**: Includes a single client computer, PC3, which is used to access services provided by the servers.


### Traffic Flow

- The Cloud-PT directs traffic from the internal network to the simulated Internet and vice versa.
- Proper routing must be configured on each router to ensure packets can reach the Cloud-PT and that return traffic can find its way back to the correct internal network.

And here we have a surprise for you! The internet is a vast place, and we've got a little something extra to show you. 

![alt text](webpage.png)
