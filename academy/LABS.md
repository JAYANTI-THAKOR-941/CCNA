# Guided practicals

## Lab 1 — Two-PC Ethernet LAN
Connect PC-A and PC-B through a switch. Set PC-A to 192.168.10.10/24 and PC-B to 192.168.10.20/24. No gateway is required for local communication. Test ping both ways; inspect link indicators and host address settings.

## Lab 2 — Subnet planning
Allocate 50, 25 and 10 usable host addresses from 192.168.20.0/24. Allocate largest first. Expected allocations: 192.168.20.0/26, 192.168.20.64/27 and 192.168.20.96/28. Calculate broadcast and usable host ranges.

## Lab 3 — Access VLAN isolation
Connect two PCs to access ports on a virtual switch. Assign both PCs addresses in the same /24. Place ports in VLAN 10 and VLAN 20. Verify that ordinary Layer 2 communication fails across VLANs. Move both into VLAN 10 and retest. Inspect VLAN membership using `show vlan brief`.

## Lab 4 — Routing between LANs
Connect two separate virtual LANs to router interfaces. Use 192.168.10.1/24 and 192.168.20.1/24 as router interface addresses. Assign each PC a matching local address and gateway. Enable the interfaces. Inspect `show ip interface brief` and `show ip route`. Verify both directions and correct a deliberately wrong gateway.

## Lab 5 — DHCP and DNS
In an isolated simulator, reserve the gateway and configure a DHCP pool in 192.168.30.0/24. Request an address from two clients. Verify distinct leases, prefix and gateway. Add a fictional DNS name lab.example.test for a local server. Compare name resolution with direct IP connectivity.

## Lab 6 — IPv6
Use documentation prefix 2001:db8:10::/64 in an isolated lab. Assign ::10 and ::20 to two hosts on the same switch. Verify local connectivity. Identify link-local and global-format addresses. IPv6 does not use IPv4 broadcast.

## Lab 7 — Troubleshooting challenge
Start from the working LAN in Lab 4. Introduce one fault at a time: disconnected cable, wrong prefix, wrong gateway, disabled interface. Record the symptom, hypothesis, evidence, correction and retest result. Restore the original layout after each fault.

## Lab 8 — Trunk design
Use two simulated switches with VLANs 10 and 20 on both. Configure a matching trunk and allowed VLAN lists. Confirm same-VLAN connectivity across the link. Change the allowed list in the simulator and observe the effect. Restore the configuration. A trunk does not provide Layer 3 forwarding between VLANs.
