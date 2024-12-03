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