
## Tasks

- [x] **Initial Router Configuration**
  
- [x] **Initial Switch Configuration**

- [x] **Server Deployments and Configuration**
  - [x] Deploy and configure the DNS server.
  - [x] Deploy and configure the SMTP server.
  - [x] Deploy and configure the iSCSI server.
  - [x] Deploy and configure the AAA server.
- [x] **Departments**
- [x] **Internet Simulation Setup**
  - Cloud-PT configured to simulate the Internet connection.

- [x] **Basic Connectivity**
  - Verified basic connectivity between Router0, Switch0, and the servers.

- [x] **VLAN Configuration**
  - [x] Create and name VLANs on the switch for each department.
  - [x] Assign switch ports to the corresponding VLANs for departmental PCs and servers.

- [x] **Inter-VLAN Routing**
  - [x] Configure Router0 with sub-interfaces for each VLAN.
  - [x] Set up the switch's port connected to Router0 as a trunk.

- [x] **Department Workstations Configuration**
  - [x] Add and configure workstations for Management/Secretariat (5 workstations).
  - [x] Add and configure workstations for Study (8 workstations).
  - [x] Add and configure workstations for Production (10 workstations).
  - [x] Add and configure workstations for Support (20 workstations, split between 2 sectors).

- [x] **DHCP Server Configuration**
  - [x] Decide whether to use Router0 or a dedicated server for DHCP.
  - [x] Set up DHCP pools for each VLAN.

- [x] **ACL and Security Configuration**
  - [x] Define ACLs to regulate traffic between VLANs.
  - [x] Optionally, create a VLAN for DMZ if needed and configure ACLs accordingly.
  - [x] Consider RADIUS configuration for centralized authentication if applicable.

- [x] **Testing and Verification**
  - [x] Test connectivity between VLANs.
  - [x]  Test DHCP configuration for dynamic IP address assignment.
  - [x] Verify ACLs to ensure appropriate access controls are in place.

- [x] **Network Services and Server Additional Configuration**
  - [x] Finalize DNS server records setup.
  - [ ] Configure the SMTP server for email simulation.
  - [ ] Document the intended setup for the iSCSI server.

- [x] **Network Documentation**
  - [x] Update the network diagram with all devices and configurations.
  - [x] Document the IP addressing scheme and VLAN assignments
  - [x] Prepare detailed configuration documentation for all network devices.
  - [x] Project Presentation Preparation

- [x] **Additional Security Measures**
  - [x] Implement strong password policies.
  - [x] Enable encryption across the network where applicable
  - [x] Future Growth and Scalability Planning
  - [x] Ensure the network design can accommodate future expansion.
