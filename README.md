# Net Practice 
system administration project designed to teach you the basics of networking .
# Key Concepts
## what is an IP address?
Ip Address stands for internet protcol address , which is a set of rules for communication between devices over the internet. it is cut up into two parts Network ID and Host ID. 

## all about IP 
there are two types of IP addresses
- IPv4 the earlier version which uses 32 bits, divided into four 8-bit blocks, uses decimal dot notation (192.422.0.1)
- IPv6 the newer version which uses 128 bits, uses hexadecimal colon notation (2001:db6::1)

## what is TCP/IP?
it stands for Transimission Control Protocol/Internet Protocol which is a set of rules that guide and allow computers to communicate on a network such as the internet

## subnetting
dividing a large network into smaller, manageable sub-networks called subnets (each with its own address range) using a subnet mask.
- suppose you have this network
  ```
  192.168.1.0/24
  ```
- you have
  ```
  192.168.1.1
  192.168.1.2
  ...
  192.168.1.254
  ```
  so all devices are in the same network
- imagien it as one large office
  ```
  Office Building
  ┌─────────────────────┐
  │ 254 employees       │
  └─────────────────────┘
  ```
  - suppose you want to separate the departments
    ```
    Building
    ├── HR
    ├── Sales
    ├── IT
    └── Finance
    ```
    this division is subnetting
  - subnetting means take some host bits and turn them into network bits
  
## subnet mask
whats the purpose of a subnet mask?
- The subnet mask helps a device determine whether another device is on the same local network or on a different network, which in turn decides whether communication is direct or must go through a router.
how does it work?
-  a device receives a packet with a destination IP. It needs to answer one question — "is this destination on my local network, or do I need to send it to a router?" to do so we can use bitwise AND
```
 (A AND mask) == (B AND mask) → same network
mask -> 1 on all network bits , 0 on all host bits
```
- in network mask when reading from left to right once a zero appears th rest of the mask will be zeros.for masks, there a only nine possible 8-bit blocks 
```
0 0 0 0 0 0 0 0 ->	0 
1 0 0 0 0 0 0 0 ->	128
1 1 0 0 0 0 0 0 ->	192
1 1 1 0 0 0 0 0 ->	224
1 1 1 1 0 0 0 0 ->	240
1 1 1 1 1 0 0 0 ->	248
1 1 1 1 1 1 0 0 ->	252
1 1 1 1 1 1 1 0 ->	254
1 1 1 1 1 1 1 1 ->	255
```
- important note we must that the first IP in the range must be reserved to identify the subnet, the last IP in the range i reserved for roadcasting messages across all devices in the subnet.
  so to calculate number of usable IPs
  ```
  2^(number of host bits) - 2
  ```

  ## what is a switch?
    A network switch connects devices within a network (often a local area network, or LAN*) and forwards data packets to and from those devices.

  ## what is a router?
    A router is a networking device that forwards data packets between different computer networks. It connects multiple packet-switched networks or subnetworks, managing traffic by directing packets to their intended IP addresses. everyrouter has an interafce for every network it conntects to
  ## interface
  - has an IP that belongs to the subnet its connected to . IP addresses of interfaces must never overlap because it would imply that multiple interfaces belong to the same network.

  
# Resources
- https://www.geeksforgeeks.org/computer-networks/role-of-subnet-mask/
- https://github.com/0xtbarkan/computer-networking
- https://github.com/tblaase/Net_Practice
