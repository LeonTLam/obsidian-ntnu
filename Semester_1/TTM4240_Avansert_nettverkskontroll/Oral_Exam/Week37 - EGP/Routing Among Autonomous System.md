Central topic is the routing protocol named [[BGP]].

Notice in designing a routing architecture, no routing update protocol can scale to allows all routers in the global internet to exchange information. Instead, routers must be divided into separate groups and routing protocols designed to operate within a group.

Three reasons for the division of routers:
* Traffic, even if it is a set of routers, the more routers added; the traffic becomes overwhelming.
* Indirect Communications. Because most routers do not share a common network and is required to hop through other networks to reach an endpoint distant from itself.
* Administrative Boundaries. The internet, networks and routers are not all owned and managed by a single entity. SPF is not always used, instead ISPs router traffic through paths that generate the most revenue or have lower financial cost.