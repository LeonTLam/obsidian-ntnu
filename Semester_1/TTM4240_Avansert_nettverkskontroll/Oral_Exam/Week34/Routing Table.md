# What is a Routing Table?
A routing table is often viewed in table format, used to determine where data packets will be directed through an Internet Protocol network. Table is usually stored inside the [[Random Access Memory (RAM)]] of forwarding devices, such as routers and network switches.

The routing table stores source and destination IP addresses in from of prefixes along with default gateway addresses and corresponding routing information.

Routing tables are typically updated dynamically through network routing protocols, but can be added manually as static entries.

# Methods of building and maintaining a Routing Table

Routing is the process of selecting the most ideal path to a network and routers, to determine the best route. There are two methods:

## Static Routing

* Manually created, managed and updated static routing table entries
* Do not change unless edited manually by network admin
* Provides granular level of control, each route is manually configured for full connectivity
* For large networks, it becomes practically impossible to add every manual entry
* Saves bandwidth and overhead because routers do not share static routes
* In a static env. the routers don't have the option to automatically switch to a better route

## Dynamic Routing

* Devices automatically build and maintain routing tables using routing protocols to exchange information about surrounding network topology. 
* Let's devices listen to network and respond to occurrences such as device failures and network congestion
* Consumes more bandwidth and overhead because routers share dynamic routes with each other
* Routers can dynamically choose better paths if there are changes in the routing infrastructure or network topology.
* Easier and simpler to configure on large networks.
* Lets routers load balance between multiple links.