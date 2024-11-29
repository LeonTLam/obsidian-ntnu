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
* /128 (a single)