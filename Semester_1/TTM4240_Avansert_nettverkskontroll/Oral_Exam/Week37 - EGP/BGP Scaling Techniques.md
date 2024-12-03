
**DO NOT** use a full mesh router network with BGP, as all routers will have active sessions with every router. Consuming an extreme amount of resources and increasing the complexity of the network.

**Two solutions**:
* Route reflector - simpler
* Confederation - more complex

# Route reflector

Reduces number of connection required in an AS.

A single router or two for redundancy, can be made as a route reflector. This way, other routers only need to be configured as a peer to them (route reflectors).

## Benefits

* Reduce IBGP mesh challenge
* Does not affect packet forwarding
* Can co-exist with normal BGP speakers
* Can simply add more reflectors for redundancy
* Easy to migrate

## Downsides

* May impose complexity if there is a single point of failure, requiring backup solutions
* Modern routers can already handle many TCP connections, requires you to have a very large network before route reflectors are necessary.

# Confederation

