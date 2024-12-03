
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

# Soft-Reconf VS Route Refresh

Use Route Refresh Capability if supported, can be found out with command:

```Command
show ip bgp neighbor
```

Uses much less memory, by utilizing the peer as **cache**

Otherwise, utilize **Soft-reconfiguration**

# Peer Groups

*Without peer-groups*, BGP would need to update changes for each BGP neighbor.
If you have a large IBGP mesh in your topology, this would require a lot of resources, to recalculate essentially the same update message.

This can be avoided by applying peer groups and grouping BGP neighbors to groups, so that updates will remain the same and applied only once per group.

This will:
* Simplify configuration
* Makes configuration less prone to error
* Makes conf. more readable
* Lower router CPU load
* Builds iBGP meshes quicker
* Allows for individual inbound policies for members
* Can be used for eBGP neighbors too