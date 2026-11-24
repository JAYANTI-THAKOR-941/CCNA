# IPv4 subnet worksheet

For conventional LANs, total addresses = 2^(32-prefix), usable hosts = total minus 2. /31 and /32 have special uses.

| Exercise | Network | Broadcast | Usable range |
|---|---|---|---|
| 192.168.1.77/26 | 192.168.1.64 | 192.168.1.127 | .65–.126 |
| 10.0.5.130/25 | 10.0.5.128 | 10.0.5.255 | .129–.254 |
| 172.16.4.19/28 | 172.16.4.16 | 172.16.4.31 | .17–.30 |

## VLSM example
Allocate 50, 25 and 10 hosts from 192.168.50.0/24:
- 50: 192.168.50.0/26 (62 usable)
- 25: 192.168.50.64/27 (30 usable)
- 10: 192.168.50.96/28 (14 usable)

Remaining addresses start at .112; the remainder is not necessarily a single aligned CIDR block.

## Student tasks
Calculate the network, broadcast, mask and usable ranges for 192.168.4.211/27, 10.20.3.45/23 and 172.16.8.100/29. Design a non-overlapping VLSM plan for 100, 40 and 12 hosts using a /24.
