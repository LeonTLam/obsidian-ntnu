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

