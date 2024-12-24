A way to map multiple private addresses inside a local network to a public IP address before transferring the information onto the internet.

```Example
Laptop connected to home wifi, requests information from the internet.
Laptop's private IP address is translated to a public IP address so the Internet knows who to respond to.
```

# Types of NAT

## Static NAT

When a local address is converted to a public one, the NAT chooses the same applied address.

## Dynamic NAT

The NAT goes through a pool of public IP addresses, and chooses a different address each time the router translates from private to public.

## PAT

"Port Address Translation", dynamic NAT that bands several local IP addresses to a singular public one. Used in i.e. organizations that want all employees' activity to use a singular IP address, often under the supervision of a network admin.