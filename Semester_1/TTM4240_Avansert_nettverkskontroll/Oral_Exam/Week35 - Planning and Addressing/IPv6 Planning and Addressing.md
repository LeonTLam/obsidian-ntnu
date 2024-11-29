# Introduction

An IPv6 address is 128 bits long, in theory there are $2^{128}$ addresses available, contra IPv4 with $2^32$ (= 4.3b).

IPv4 planning requires the network managers to be efficient with the available addresses. If you where to apply for an IPv6 address range, most ISP's will provide a /48 prefix ($2^{80}$ addresses) which is hardly an issue for efficiency.

# Structure of IPv6 Addresses

IPv6 addresses are four times longer than IPv4 addresses. The length of IPv6 is so long that it is formatted on the **hexadecimal system**. 

Each digit in the hexadecimal system is equivalent to 4 bits, an IPv6 address consists therefor of 32 hexadecimal digits:

```Notation
2001:0db8:0000:0000:0000:0000:0000:0001
```

It is impractical to record all zeroes, leading zeroes can be dropped for each group of digits:

```Shortened
2001:db8:0:0:0:0:0:1
```

One, and only one, series of zeroes and colons may also be abbreviated as two colons.

```Abbreviated
2001:db8::1
```

## Prefixes: Grouping Addresses

```Example
2001:db8::/32
```

Contains all addresses from

```Through
2001:0db8:0000:0000:0000:0000:0000:0000
to
2001:0db8:ffff:ffff:ffff:ffff:ffff:ffff
```

```Through
2001:db8:1234::/64
contains all addresses from
2001:0db8:1234:0000:0000:0000:0000:0000
to
2001:0db8:1234:ffff:ffff:ffff:ffff:ffff
```

# /64 Subnets

IPv6 does not have a fixed structure like Class A/B/C, however they should be /64. Very small subnets, such as p-to-p link, use the same size IPv6 address block as very large subnets.

# Assigning Address Blocks

Original recommendation for assigning IPv6 address space to end users was as follows:

* /48 (65 536 subnets) in general case, except for very large subscribers
* /64 (single subnet) when it known that one and only one subnet is needed
* /128 (a single address) when it is absolutely known that one and only one device is connecting

It is recommended against giving out single addresses. /48 is much more than a home user needs, but a /64 only allows for a single subnet, which may be limiting. In the future, a /56 or /60 may be more appropriate for consumers. 

# Basic Structure of the Address Plan

With IPv6 protocol, there so many available addresses that we can create one or more primary subnets. We can for example assign:

* Per use type
* Then by location
* remaining bits to another purpose

```Example
	2001:db8:1234: |L|L|L|L|T|T|T|T|B|B|B|B|B|B|B|B|::/64
```

* 4 bits are assigned to a location (L)
* 4 bits assigned to a use type (T)
* Remaining 8 bits (B)

16 locations can be addressed, with each location having 16 allocatable use types. 8 bits left to a number of maximum 256 different subnets for each location and use type combination.

## Recommendation

Applying the use type first makes it much easier to implement a 


