
**Applying new policies**

*Problem*:
* Hard BGP peer reset (clear) required after every policy change because the router does not store prefixes that are denied by a filter.
* Hard BGP peer clearing consumes CPU and affects connectivity for all networks
	* Causes unnecessary route flap, very bad for networks with million routes.

*Solution*:
* Soft-reconfiguration or route refresh
* Soft reset

## Soft-reconfiguration

Achieved by create an additional table in the ongoing BGP session. Reread new incoming configuration, discarding old config and keep running BGP session.

* Enables new policy activation without needing to tear down and restarting peering session
* Per-neighbor basis
* Uses **more memory** to keep prefixes whose attributes have been changed or have not been accepted.

## Route Refresh Capability

Non disruptive policy changes
No configuration needed
No additional memory used
Requires peering routers to support **route refresh capability** 

```Command
clear ip bgp x.x.x.x in 
```
Tells peer to resend full BGP announcement, rebuilds local BGP table.

# Preferabilit