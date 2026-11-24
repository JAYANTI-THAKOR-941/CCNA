# Packet Tracer lab workbook

## Lab 1 — Two-PC LAN
Add two PCs and a switch. Connect each PC to a switch access port. Configure PC1 192.168.10.10/24 and PC2 192.168.10.20/24. Ping PC2 from PC1. Disconnect one cable and repeat. Expected: reachable with active links, failure when disconnected.

## Lab 2 — Access VLANs
Use a switch with two PCs in VLAN 10 and one PC in VLAN 20. Assign the first two addresses in 192.168.10.0/24 and the third in 192.168.20.0/24. On the virtual switch, create vlan 10 and vlan 20, select the appropriate interface, set switchport mode access and switchport access vlan 10 or 20. Verify show vlan brief. Same-VLAN PCs should communicate; different VLANs require routing.

## Lab 3 — Trunk verification
Connect two virtual switches. Create VLAN 10 on both and configure their inter-switch ports in trunk mode with VLAN 10 permitted. Connect one PC in VLAN 10 to each switch. Verify show interfaces trunk and ping. Remove VLAN 10 from the permitted list on one side and observe the effect. Restore the configuration.

## Lab 4 — Directly connected routing
Connect two PCs to separate router interfaces. Use networks 192.168.10.0/24 and 192.168.20.0/24. Router interfaces use .1 in each subnet, PCs use .10, and gateways point to their local router interfaces. Enable router interfaces with no shutdown. Verify show ip interface brief and show ip route, then ping across networks.

## Lab 5 — Static routing
Use two routers with a 10.0.0.0/30 transit network, R1 .1 and R2 .2. Use the LAN networks from lab 4, one per router. Add a route to the remote LAN using the neighboring router's transit IP, on both routers. Verify the routing table, return path and ping. Remove a route and explain failure.

## Lab 6 — DHCP
Use an isolated virtual server with a pool 192.168.30.100–149/24, gateway 192.168.30.1 and DNS server as appropriate for the lab. Set two PCs to DHCP and inspect distinct leases. Ensure no overlapping static addresses.

## Lab 7 — IPv6 LAN
Assign 2001:db8:30::10/64 and 2001:db8:30::20/64 to two virtual PCs on one switch. Test IPv6 ping. Explain link-local addresses and why IPv6 does not use broadcast.

## Lab 8 — Troubleshooting
In a working lab, introduce one fault at a time: disabled port, incorrect prefix, wrong gateway, or incorrect VLAN. Observe symptoms, check physical/link state, verify addressing, then routing. Restore baseline and document the result.

These expected outcomes assume compatible device models and correct configurations. They have not been executed in Packet Tracer here.
