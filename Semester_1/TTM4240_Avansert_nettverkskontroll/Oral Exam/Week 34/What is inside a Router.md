Figure 1, high level view of generic router architecture. Four router components can be identified.
![[Router architecture.png]]

* **Input ports**. 
	* Performs physical layer function of terminating an incoming physical link at a router. 
	* Also performs link-layer functions needed to interoperate with the link layer at the other side of the incoming link..
	* Most crucially, a lookup function performed at input port. Forwarding table is consulted to determine router output port to which an arriving packet will be forwarded via. the switching fabric.
* *Æ