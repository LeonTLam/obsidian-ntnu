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

* netA requires a /23 subnet mask, giving space for 512 addresses
* netB requires a /29 subnet mask, giving space for 6 addresses, 1 for network ID and 1 for broadcast ID
* netC requires a /30 subnet mask, giving space for 2 addresses, --**--
* netD requires simply a /32 subnet mask, since we are working with a router loopback (no need for network ID and Broadcast ID)

Furthermore, we now assign the subnets to the network 192.168.5.0/24 and begin with the largest subnet.

* netA 192.168.5.0/23 (range from 5.0 to 6.255)
* netB 192.168.7.0/29 (range from 0 to 7)
* netC 192.168.7.8/30 (range from 8 to 11)
* netD 192.168.7.12/32 (range at 12)
```

## Summarization

Summarizing IP addresses ensure that no entries for child routes are outputted. A normal routing table and routing advertisement would have sent out i.e. seven routes. With summarization, all seven routes are summarized back to the HQ as a single route. 

This is quite useful for networks that are planned to scale and especially networks with contiguous IP spaces.

## IP Multicast

Bandwidth conservation technology that reduces traffic and server loads by allowing a single stream of information on the network to be received by multiple users (thousands i.e.)

IANA has reserved the range of 239.0.0.0/8 as Administratively Scoped addresses for use in private mutlicast domains..

## Process of Creating an Addressing Plan

```
1. Define Addressing Standards
2. Plan Range
3. Allocate IP space
4. Document plan
```

Within each subnet range, the plan should account for:
* Subnet sizes
* Subnet assignment
* Static address assignments for network devices
* Dynamic address assignments

### Procedure 1 - Define Addressing Standards

**STEP 1**: Create standards for IP address assignments within each subnet range. May include:

* VLANs can be created to match the third octet of the IP subnet plus 100. Example, IP x.x.71.x is assigned VLAN 171
* Routers, gateways and Hot Standby Router Protocol (HSRP) virtual addresses within a subnet are assigned the first available addresses within the range.
* Printers and other fixed address assignments.
* Dynamic address ranges for Dynamic Host Control Protocol (DHCP). Example, all user subnets may be /24 subnets with 253 available address assignments for end hosts.
* Routers may be assigned the .2 and .3 addresses, and HSRP address assigned the .1 address.
* Printers may be assigned the .5 through .9 addresses.
* DHCP may range from .10 through .250 addresses.

**STEP 2**: Define a consistent, structured naming convention and DNS for devices.

* Create a consistent access point to routers for all network management information related to a device
* Reduce the opportunity for duplicate IP addresses
* Create simple identification of a device showing location, device type and purpose
* Improve inventory management by providing a simpler method to identify network devices

**STEP 3**: Identify DHCP ranges and add them to DNS, inc. the location of the users. 

**STEP 4:** Document all standards that you develop and reference them on all network engineering plan documents to help ensure consistent deployment.

### Procedure 2 - Plan Range

There is no incorrect private subnet to allocate, but some choices provide more flexibility than others.

**STEP 1:** Determine which address space to use by evaluating all of the user and server requirements. Consider the following examples.

* 192.168.0.0 range is used by many companies and network equipment vendors. This address range has a lower number of host addresses available, which may become an issue as an organization grows or when a merger occurs with another company using the same range.
* If you have the luxury, consider the 10.0.0.0 range to allow for more flexibility.
* In many cases, organizations may have multiple different address RFC 1918 spaces in their network. To simplify configuration and troubleshooting, it is easier to work with one RFC 1918 space and use summarization. Using multiple IP ranges from different address spaces is not a problem if the addressing plan is well documented.
* Whatever address space is selected or inherited, there may be an advantage to start somewhere other than beginning of the range when choosing network numbering. When merging with another company using same IP addressing space, it is advisable to not start at the beginning of the range, to decrease the change of address conflicts.

### Procedure 3 - Allocate IP Space

Clearly define the size of the IP space with public addresses as it is available only in finite amount.
Keep in mind:

* Private addresses are not constrained
* For ease of use, /24 mask should be used as a minimum for user subnets
* End devices always grow in number, no need to set a low number limit of private addresses
* WAN connections require smaller IP spaces

**REMEMBER** to reserve a subnet for physical security, facilities, all production networks in the demilitarized zone (DMZ), Remote Access (VPN), Network Management, and Loopback addresses