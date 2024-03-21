# Current ASA Config

##### Interfaces:
- Ethernet 0/0 linked to VLAN 2 name **outside** (192.168.2.2/24) security-level = 0
- Ethernet 0/1 linked to VLAN 1 name **inside** (192.168.1.3/24) security-level = 100
- Ethernet 0/2 linked to VLAN 10 name **dmz** (192.168.10.1/24) security-level = 50
##### VLAN Modes:
- Ethernet 0/0 switchport mode access
- Ethernet 0/1 switchport mode access
- Ethernet 0/2 switchport mode access
##### Routing Table:
- Gateway of last resort is 192.168.2.1 to network 0.0.0.0
- C 192.168.1.0 255.255.255.0 is directly connected, inside, Vlan1
- C 192.168.2.0 255.255.255.0 is directly connected, outside, Vlan2
- C 192.168.10.0 255.255.255.0 is directly connected, dmz, Vlan10
- S* 0.0.0.0/0 [1/0] via 192.168.2.1
##### NAT:
- (inside) to (outside) source dynamic LAN interface
##### Access Control Lists:
- access-list ASA extended permit tcp any any
- access-list ASA extended permit icmp any any
