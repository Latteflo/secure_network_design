# secure_network_design

## Completed Tasks

- [x] **Initial Router Configuration**
  - Configured with IP `192.168.1.1`.
  
- [x] **Initial Switch Configuration**
  - Cisco 2960-24TT Switch0 is connected to Router0.

- [x] **Server Deployments and Configuration**
  - DNS Server: IP `192.168.1.10`.
  - SMTP Server: IP `192.168.1.11`.
  - iSCSI Server: IP `192.168.1.12`.

- [x] **Internet Simulation Setup**
  - Cloud-PT configured to simulate the Internet connection.

- [x] **Basic Connectivity**
  - Verified basic connectivity between Router0, Switch0, and the servers.


## To-Do List

- [ ] **VLAN Configuration**
  - [ ] Create and name VLANs on the switch for each department.
  - [ ] Assign switch ports to the corresponding VLANs for departmental PCs and servers.

- [ ] **Inter-VLAN Routing**
  - [ ] Configure Router0 with sub-interfaces for each VLAN.
  - [ ] Set up the switch's port connected to Router0 as a trunk.

- [ ] **Department Workstations Configuration**
  - [ ] Add and configure workstations for Management/Secretariat (5 workstations).
  - [ ] Add and configure workstations for Study (8 workstations).
  - [ ] Add and configure workstations for Production (10 workstations).
  - [ ] Add and configure workstations for Support (20 workstations, split between 2 sectors).

- [ ] **DHCP Server Configuration**
  - [ ] Decide whether to use Router0 or a dedicated server for DHCP.
  - [ ] Set up DHCP pools for each VLAN.

- [ ] **ACL and Security Configuration**
  - [ ] Define ACLs to regulate traffic between VLANs.
  - [ ] Optionally, create a VLAN for DMZ if needed and configure ACLs accordingly.
  - [ ] Consider RADIUS configuration for centralized authentication if applicable.

- [ ] **Testing and Verification**
  - [ ] Test connectivity between VLANs.
  - [ ] - Test DHCP configuration for dynamic IP address assignment.
  - [ ] Verify ACLs to ensure appropriate access controls are in place.

- [ ] **Network Services and Server Additional Configuration**
  - [ ] Finalize DNS server records setup.
  - [ ] Configure the SMTP server for email simulation.
  - [ ] Document the intended setup for the iSCSI server.

- [ ] **Network Documentation**
  - [ ] Update the network diagram with all devices and configurations.
  - [ ] Document the IP addressing scheme and VLAN assignments
  - [ ] Prepare detailed configuration documentation for all network devices.
  - [ ] Project Presentation Preparation

- [ ] **Additional Security Measures**
  - [ ] Implement strong password policies.
  - [ ] Enable encryption across the network where applicable
  - [ ] Future Growth and Scalability Planning
  - [ ] Ensure the network design can accommodate future expansion.

Let's not forget to update the Readme file too!