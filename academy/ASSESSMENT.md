# Networking knowledge check

Answer before reading the key.

1. Which OSI layer forwards IP packets?
2. What is the network address of 192.168.10.70/26?
3. How many conventional usable host addresses does /27 provide?
4. What is the broadcast address of 192.168.20.64/27?
5. Why does a host need a default gateway?
6. What is an access VLAN?
7. What problem does STP solve?
8. What does DHCP provide?
9. What is the difference between DNS and ARP?
10. What protocol provides ordered reliable byte streams?
11. How many bits does IPv6 use?
12. Why test return paths when troubleshooting routing?

## Answer key
1. Network layer (Layer 3).
2. 192.168.10.64.
3. 30.
4. 192.168.20.95.
5. To send traffic outside its local subnet.
6. A logical Layer 2 broadcast domain associated with an access port.
7. Layer 2 forwarding loops.
8. Address leases and configuration such as prefix, gateway and DNS.
9. DNS resolves names; ARP maps local IPv4 addresses to link-layer addresses.
10. TCP.
11. 128.
12. Successful communication requires responses to reach the source as well.
