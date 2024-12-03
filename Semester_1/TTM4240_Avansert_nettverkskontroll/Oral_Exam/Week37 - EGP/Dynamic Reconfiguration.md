
**Applying new policies**

*Problem*:
* Hard BGP peer reset (clear) required after every policy change because the router does not store prefixes that are denied by a filter.
* Hard BGP peer clearing consumes CPU and affects connectivity for all networks
	* Causes unnecessary route flap, very bad for networks with million routes.

*Solution*:
* Soft-reconfiguration or route refresh
* Soft reset