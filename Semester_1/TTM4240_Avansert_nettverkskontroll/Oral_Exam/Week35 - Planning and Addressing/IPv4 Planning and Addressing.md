*An IP address uniquely identifies a device on an IP network.*

If you don't have a laid out plan on IP addressing, it will become confusing to allocate, recycle and document IP addresses.

IP addressing is core to network design and provides the base for all other network and user services.

By following recommended IP address management standards, you can avoid:
* Overlapping or duplicate subnets
* Unsummarized routes in a network
* Duplicate IP address device assignments
* Wasted IP address space
* Unnecessary complexity

# IPv4 Addressing Basics

IP version 4 addresses are **32 bits** in length and communicated in dotted decimals.

The 32 binary bits are:
* Divided into a network portion and host portion
* Broken into four octets (1 octet = 8 octet). Each octet can be converted to binary

```
The IP: 10.10.16.1

Breakdown (4 octets):
* 10
* 10
* 16
* 1
```

## IP Address Classes

**Class A**: First octet is the network portion
**Class B**: First two octets are the network portion
**Class C**: First 3 are the network portion

Class A has 3 octets for the host portion of the address. Inefficient use of address space, since available Layer 2 technologies cannot easily support this many hosts on a single subnet.

![[Address_Classes.png]]

## Private IP Addressing

The **Internet Assigned Numbers Authority** (IANA) has reserved a number of IPv4 network ranges as private. These network addresses are routed in the public internet as defined in RFC 1918.

These network ranges (RFC 1918) are reserved for organizations that want to build an internal network infrastructure based on TCP/IP but either do not have or do not want to use public IP space.

**RFC 1918** space includes following three blocks of IP address space:
* 10.0.0.0 - 10.255.255.255 (10.0.0.0/8), allows greatest flexibility with the equivalent of 255 Class B
* 172.16.0.0 - 172.31.255.255 (172.16.0.0/12) allows for 16 Class B address spaces
* 192.168.0.0 - 192.168.255.255 (192.168.0.0/16) allows for one Class B address space

By mutually understanding these ranges as private an non-routable in the internet, multiple organizations can utilize these ranges internally without causing conflict with public internet addresses. If these ranges where to be routed publicly, it would simply be filtered out by the internet provider.

## Subnetting

Subnetting allows one to create multiple logical networks that exist within a single Class A, B or C network. If you do not create subnets, you would only have a SINGLE network from your Class A, B or C network. Essentially, a lonely network with a single host.

Each data link on a network must have a unique network address, with every host on that link being a member of the same network. If you break down a major network (Class A, B or C) into multiple subnets, you would have a network of interconnected subnetworks. Each data link on this network would then have a unique network/subnetwork ID.

``` Example
192.168.5.0 255.255.255.224 (range 0 to 31)
192.168.5.32 255.255.255.224 (range 32 to 63)
192.168.5.63 255.255.255.224 (range 64 to 95)
...
192.168.5.224 255.255.255.224 (range 224 to 255)
```

## Variable Length Subnet Masks (VLSMs)

VLSMs allows you to use different masks for each subnet, this uses address space efficiently. For private address space, it is rarely necessary to shrink below /24 subnets as space is plentiful.

VLSMs is useful to:
* Create a larger subnet of more than 255 host addresses.
* Create very small subnets for WAN links
* Configure loopback addresses

``` VLSM Example
Given the 192.168.5.0/24 network and requirements below. Develop a subnetting scheme with the use of VLSM:

* netA must support 330 hosts
* netB must support 6 hosts for a p-to-p WAN link supporting Hot Standby Router Protocol (HSRP)
* netC must support 2 hosts for a T1 circuit to a remote site
* netD must support a single address for a router loopback

First step is to determine what mask allows the required number of hosts.

* netA requires 
```
