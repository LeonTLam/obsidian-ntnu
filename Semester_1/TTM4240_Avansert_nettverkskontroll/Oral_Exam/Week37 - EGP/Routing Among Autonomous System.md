Central topic is the routing protocol named [[BGP]].

Notice in designing a routing architecture, no routing update protocol can scale to allows all routers in the global internet to exchange information. Instead, routers must be divided into separate groups and routing protocols designed to operate within a group.

Three reasons for the division of routers:
* Traffic, even if it is a set of routers, the more routers added; the traffic becomes overwhelming.
* Indirect Communications. Because most routers do not share a common network and is required to hop through other networks to reach an endpoint distant from itself.
* Administrative Boundaries. The internet, networks and routers are not all owned and managed by a single entity. SPF is not always used, instead ISPs router traffic through paths that generate the most revenue or have lower financial cost.

# Understanding a practical limit on a group size

Understanding the size of a network requires one to understand the traffic a specific protocol will generate. There are two issues: Delay and Overhead:

**Delay**: Convergence time, the maximum delay until all routers are informed about a change.

```Example
Distance-vector protocol, each routers must receive new information, update its FIB, and then forward the information to its neighbors.
In a network with N routers in a linear topology, N steps are required. Then, N must be limited to guarantee rapid distribution.
```

**Overhead**: Each router that participates in a routing protocol must send messages. The larger participation means more routing traffic. If routing messages contain list of possible destinations, size of each message grows as the number of routers and networks increase. Ensure that size of routing traffic is a small percentage of total traffic, size of routing messages must be limited. 

It is not advisable to determine size of a network solely on routing architecture, instead they must implement traffic monitoring and listen passively to a network to determine the amount of routers that should participate in a single routing protocol.

