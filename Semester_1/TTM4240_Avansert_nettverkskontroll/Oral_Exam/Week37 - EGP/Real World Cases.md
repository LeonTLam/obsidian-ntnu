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

## Longest Prefix 