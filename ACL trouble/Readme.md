How ~~the fuck~~ do you make this work?

Create the access list like so:
access-list 10 permit host 200.200.10.11
then with go into the interface where you want those rules applied and specify if the traffic is coming in through there or out it's pretty self explanatory.

If I want to check traffic from the inside then I go into my "inside" interface and I put "ip access-group 10 in" If I wanted to check it once it gets out I would do the same on my "outside" interface.

So here's what I have for now (for testing purposes and it works perfectly):
- `access-list 10 permit host 200.200.10.11`
- `access-list 10 permit host 200.200.10.12`
- `access-list 10 deny any`
- `int g0/1`
- `ip access-group 10 in`

I will now recreate it for our use case:
- `access-list 20 permit host 192.168.1.2` (dhcp)
- `access-list 20 permit host 8.8.0.0` (google stuff)
- `access-list 20 permit host 150.1.0.0` (other internet stuff)
- `access-list 20 permit host 200.200.10.0` (DMZ)
- `access-list 20 deny host 192.168.20.0` (LAN subordinates)
- `access-list 20 deny host 192.168.30.0` (LAN subordinates)
- `int vlan 40`
- `ip access-group 20 out`
- `exit`
- `do wr`
- `exit`
- `wr me`
---
Working with packet tracer be like:
- `access-list 20 permit 8.8.0.0`
The response:
4. The outgoing port has an outbound traffic access-list with an ID of 20. The device checks the packet against the access-list.
5. The packet does not match the criteria of any statement in the access-list. The packet is denied and dropped by default.
Ok then I'll explicitly allow this exact ip in the access-list and let's see what happens.\
Me: `access-list 20 permit host 8.8.8.8`\
Packet Tracer: ping successful

Well I guess I did something wrong. Maybe I have to include "host" before a network address even though in their syntax it explicitly says that host is for "a SINGLE host address" but you never know let's try.

I have edited my config to test that theory and cisco said fuck you.
