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