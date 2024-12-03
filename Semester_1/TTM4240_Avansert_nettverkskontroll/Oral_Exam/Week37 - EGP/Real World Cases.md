Not all challenges are technical. 

# General costs of BGP

**CPU** costs in
* BGP session establishment
* Router selection
* Routing information processing
* Handling of routing updates

**Router memory** costs
* install routes and handle multiple paths associated with routes.

**System Complexity**
* Local AS with multiple routers have to each handle IBGP sessions with N-1 routers.
	* Consumes a lot of resources from each routers, especially during session establishment and during periods of **heavy router flapping** (path going up and down).
* Policy management

**Security**
* Filter configuration management

# IP hijacking

A party advertises incorrect routing information, convincing routers across the globe to send traffic on geographically absurd paths.

China in 2010 did exactly this and routed about 15% of the internet's traffic through servers located in China. The incident affected traffic to and from even confidential data of the US.

## Longest Prefix Wins

A better prefix can be misused to reroute traffic through itself. 

## What one can do

For public peering, **filter** EBGP routes inbound and outbound
* Block own address space inbound
* Block RFC 1918 private space both inbound and outbound
* Block well-known not used addresses both inbound and outbound

Use **prefix-lists** for route-filtering when possible