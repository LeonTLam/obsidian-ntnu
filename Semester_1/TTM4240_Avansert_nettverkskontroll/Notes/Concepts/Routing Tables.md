Set of rules, often viewed in table format. 
Used to determine where data packets traveling over an Internet Protocol (IP) network will be directed.

```
**Destination**      **Subnet mask**         **Interface**
 128.75.43.0         255.255.255.0           Eth0
 128.75.43.0         255.255.255.128         Eth1
 192.12.17.5         255.255.255.255         Eth3
 default                                     Eth2
```

A routing table will contain information necessary to forward a packet along the best path toward its destination. Each entry in a routing table may consist of the following:

* *Network ID:* 
	The network ID or destination corresponding to the route
* *Subnet Mask:*
	Mask used to match a destination IP address to the network ID
* *Next hop:*
	IP address to which the packet is forwarded
* *Outgoing interface:*
	Outgoing interface the packet should go out to reach the destination network
* *Metric:*
	Often used to indicate the minimum number of hops to the network ID.