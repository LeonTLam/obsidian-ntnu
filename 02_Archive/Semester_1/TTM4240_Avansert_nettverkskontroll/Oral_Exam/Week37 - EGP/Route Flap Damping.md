
**Route flap**
* going up and down of path or change in attribute
	Happens by a BGP route going up and down (WITHDRAW) followed by and UPDATE
	Does not relate to an eBGP neighbor going up and down (called interface flap)
* This will influence the whole internet
* Wasting CPU resources

Damping will aim to reduce the scope of route flap propagation

## Requirements

* Fast convergence for normal route changes
* History can predict future behaviors
* Suppress oscillating routes 
* Advertise stable routes

## Operation

* Add penalty (1000) for each flap
	* Change in attribute gets penalty of 500
* Exponenttially decay penalty
	* Half life determines decay rate
* Penalty above suppress-limit
	* do not advertise route to BGP peers
* Penalty decayed below reuse-limit
	* Re-advertise route to BGP peers and penalty reset to zero when it is half of reuse-limit (at some point in time)