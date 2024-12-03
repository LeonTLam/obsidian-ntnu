# Topics

* Autonomous Systems
* Border Gateway Protocol (IGBP and eBGP)
	* Error handling
	* Message Type
		* BGP Open message within Ethernet link layer frame, through TCP
		* Example of two edge routers speaking in BGP establishing a BGP session
* BGP scalability
	* Full meshed BGP network
		* Excessive resource costs and unnecessary complexity
		* Solution: Route Reflector
			* Redundancy by configuring another router as a route reflector
	* Further improvements to BGP
		* MPLS
			* reducing the load from large routing tables, by using labels within the MPLS domain
			* Define explicit routes for prioritized traffic using LSPs, instead of BGP's "Shortest AS path".
			* Optimize traffic latency, bandwidth or reliability.
			* Multiple LSPs between endpoints 