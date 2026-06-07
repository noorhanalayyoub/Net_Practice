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
  ## subnetting means take some host bits and turn them into network bits
## subnet mask
whats the purpose of a subnet mask?
- The subnet mask helps a device determine whether another device is on the same local network or on a different network, which in turn decides whether communication is direct or must go through a router.
how does it work?
-  a device receives a packet with a destination IP. It needs to answer one question — "is this destination on my local network, or do I need to send it to a router?" to do so we can use bitwise AND
```
 (A AND mask) == (B AND mask) → same network
mask -> 1 on all network bits , 0 on all host bits
```


# Resources
- https://www.geeksforgeeks.org/computer-networks/role-of-subnet-mask/
      
