# Secure Network Design Project – No Nonsense Network Know-How

## So, What's the Big Idea?

Hey there! You've stumbled upon our humble lair where we're busy crafting a network that's secure enough to make the anyone envious. This isn't just any network; it's a modern marvel that balances cost with fortress-level security.

### Team Effort

3 brainiacs/group:
- **Teddy**: The visionary, always three steps ahead.
- **Esaü**: The executor, turns plans into reality.
- **Flo**: The detailer, fine-tunes everything to perfection.

## The Lowdown on Our Project

We've got a mission: to yank a client’s office into the 21st century by networking the heck out of it.
 
We’re talking about a setup that screams efficiency(!), oozes security(!!!), and doesn’t break the bank (...too much).

## Here's How We Roll

- **Simulate to Dominate:** Using Cisco Packet Tracer to get a bird's-eye view of our handiwork.
- **Documentation Domination:** Writing up stuff so well, it'll be crystal clear years from now.
- **Security Obsession:** We're basically digital ninjas keeping the bad guys at bay.
- **Show and Tell:** We’ll explain our moves so even our grannies would get it.

## The Game Plan

- **Network Not-So-Trivial Pursuit:** Does our Packet Tracer simulation actually work? You betcha.
- **The Blueprint (Packet Tracer File):** Check out our `.pkt` to see how we roll.
- **The Big Picture:** Are we seeing the forest for the trees?
- **Fortress Foundations:** Did we go all medieval with the security? Like a digital moat.

## The Nuts and Bolts (But Mostly Wires)

Our network’s a thing of beauty. There's a sketch below that shows all the connections, kind of like a family tree but for computers.

### The Setup

Our setup’s got more layers than a lasagna. Here’s the breakdown:

- **[Routers](documentation/Routers/Routers.md):** The traffic cops of the network.
- **[Switches](documentation/Switches/Switches.md):** The traffic directors of the network.
- **[Servers](documentation/Servers/Servers.md):** The network’s workhorses.
- **[Cloud](documentation/Servers/Cloud/Cloud.md):** The internet, because what’s a network without the internet?
- **[VLANs](documentation/Servers/VLAN/VLAN.md):** The network’s neighborhoods, each with its own purpose.
- **[AAA](documentation/Servers/AAA/AAA.md):** The network’s bouncer, making sure only the right folks get in.
- **[DMZ](documentation/Servers/DMZ/DMZ.md):** The network’s no-man’s-land, where the bad guys get stuck.

### The Plot (Sector Breakdown)
- **Management/Secretariat:** 5 desks where the magic happens.
- **Study:** 8 desks for scholarly pursuits.
- **Production:** 10 desks for making dreams come true.
- **Support:** 20 desks, divided by two, for saying "Have you tried turning it off and on again?"

### Floor plan
  - **[Routers](documentation/Routers/Routers.md):** We love them, we hate them, but we can't live without them. 
  - **[Switches](documentation/Switches/switches.md):** The switch that makes it all happen  (and sometimes not happen).
  - **[Servers](documentation/Servers/servers.md):** DNS, SMTP,AAA and iSCSI servers are all in the mix.
  - **[Cloud]():** Our internet simulation, because we can't have a network without the internet.
  - **[VLANs](documentation/VLAN/VLAN_docu):** We've got VLANs for days, each with its own purpose.
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


### Security (aka The Bouncer)
This was quite a treat! We've got security measures that are tighter than a drum, and because Cisco Packet Tracer is our long-time friend (and sometimes foe), we've tried the inplementation of a firewall that turned up to be a bit of a diva. As such we had to take a step back and re-evaluate our approach.

 Why? Because we can only simmulate and not recreate and simmulation happens matrix style - `we can't just bend the rules of the matrix, we have to play by them.`

 Our pick of choice for the firewall was the Cisco ASA 5505, but we had to make do with the Cisco NR router.
 To this we implemented the following security measures:
- **[RADIUS and TACACS +](<[text](documentation/AAA/AAA.md)>) :** It's like the club's VIP list, but for network access.

## The Fine Print
- **[DMZ Drama](<dmz trouble/asa_config.md>):** We considered a DMZ, but we're still mulling it over.   
- **CPT Limitation Limbo:** We hit a snag, but we’re crafty and we’ll figure it out...eventually.

## The Grand Finale
We’re not done yet! We’ve got a few more tricks up our sleeves before we call it a day. Stay tuned!

## Shout-Outs
- Props to BeCode for throwing down the gauntlet!
- High-fives to all our brainy teammates for making this happen!

