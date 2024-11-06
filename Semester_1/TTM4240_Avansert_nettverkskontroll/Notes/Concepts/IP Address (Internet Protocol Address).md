Network address for a source/destination.

How an IP address works in a web-surfing scenario:
* A device directly requests the Service Provider which then grants the device access to the web.
* An IP Address is assigned to the device from the given range available.
* The internet activity goes through your service provider, and THEY route it back to you, using your IP address.
* If the router for the devices is turned off and reset, the IP address can change.
* When the device leaves the router, the IP address to the device changes as it changes when switching networks.

**Two types of IP Address**

1. *IPv4:* Internet Protocol version 4. Consists of 4 numbers separated by dots. Each number ranging from 0-255 in decimal numbers. From a computer's perspective, the numbers are only 0's and 1's. Therefore, in binary, the range (0-255) is written as (00000000 - 11111111). Each group of 4 numbers is represented by an 8-digit binary digits, so the whole IPv4 binary address can be represented by 32-bits of binary digits. There can be a total of 2^25 unique sequence of bits, in other words, IP's assigned to 4,294,967,296 devices.

``` Example
189.123.123.90
```

**Classes of IPv4 Address**

| IP Class | Address Range | Max number of networks                 |
| -------- | ------------- | -------------------------------------- |
| Class A  | 1-126         | 126(2^7-2)                             |
| Class B  | 128-191       | 16384                                  |
| Class C  | 192-223       | 2097152                                |
| Class D  | 224-239       | Reserve for multitasking               |
| Class E  | 240-254       | Reserved for Research and Development. |
*0.0.0.0* is a **Non-routable** address, indicates an invalid or inapplicable END-user address.

A [[Loopback Address]] is a distinct reserved IP range from 127.0.0.0 to 127.255.255.255, with the exception of 127.255.255.255 being the broadcast address for 127.0.0.0/8.

2. *IPv6:* Since the issue of running out of IP's on IPv4 exists, the world is gradually making its way to IPv6 addresses. It is written as a group of 8 hexadecimal numbers separated with colons, a 128-bit IP address. In other word, a total of 2^128 devices can be assigned with unique addresses.

```Example
2011:0bd9:75c5:0000:0000:6b3e:0170:8394
```

