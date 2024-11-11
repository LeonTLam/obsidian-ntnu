Figure 1, high level view of generic router architecture. Four router components can be identified.
![[Router architecture.png]]

* **Input ports**. 
	* Performs physical layer function of terminating an incoming physical link at a router. 
	* Also performs link-layer functions needed to interoperate with the link layer at the other side of the incoming link..
	* Most crucially, a lookup function performed at input port. Forwarding table is consulted to determine router output port to which an arriving packet will be forwarded via. the switching fabric.
* **Switching fabric**.
	* Connects router's input ports to its output ports. Completely contained within the router - network inside a router.
* **Output ports**.
	* Stores packets received from the switching fabric and transmits these on the outgoing link by performing link-layer and physical-layer functions.
	* When a link is bidirectional, an output port will typically be paired with the input port for that link on the same line card.
* **Routing processor**.
	* Performs control-plane functions. 
	* In traditional routers, it executes the routing protocols, maintains routing tables and attached link state information and computes the forwarding table for the router.
	* In SDN routers, the routing processor is respons. for commun. with the remote controller in order to receive forwarding table entries computed by the remote controller.
	* 