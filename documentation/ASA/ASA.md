#  ASA config 

For educational purposes, we have an ASA firewall (please check the asa.pkg file)

![alt text](asa.png)

**The reason it is not integrated in the big network is because of the limitations of the simulation software.**

We used the following configuration:

#### Interfaces:
- g 1/1 name **outside** `192.168.2.2/24` security-level = 0
- g 1/2 name **dmz** `192.168.10.1/24` security-level = 50
- g 1/3 name **inside** `192.168.1.3/24` security-level = 100


#### Routing Table:

- Gateway of last resort is not set
- C `192.168.1.0` `255.255.255.0` is directly connected, inside, GigabitEthernet1/3
- C `192.168.2.0` `255.255.255.0` is directly connected, outside, GigabitEthernet1/1
- C `192.168.10.0` `255.255.255.0` is directly connected, dmz, GigabitEthernet1/2


#### NAT:
- object network LAN 
	- subnet `192.168.1.0` `255.255.255.0` 
		- nat (inside,outside) dynamic interface
#### Access Control Lists:
- access-list OUTSIDE extended permit icmp any any echo-reply
- access-list OUTSIDE extended permit icmp any any unreachable
#### Access Group:
- access-group OUTSIDE in interface dmz
- access-group OUTSIDE out interface inside
