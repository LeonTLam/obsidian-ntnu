**Border Gateway Protocol (BGP)**: is used to exchange reachability information in the Internet.

When a pair of **ASes** agree to use **BGP** to exchange routing information, each AS must designate a router that will speak BGP on its behalf. These pair of routers are known as **BGP peers** of one another. It is essentially necessary that both routers are near the border (edge routers) of the AS.

# EBGP

Exterior or External Border Gateway Protocol, learn routes of external AS

## Failure Handling

If a peering-link using eBGP goes down, 
the TCP connection breaks (BGP session terminated)
and the BGP routers are removed.

# IBGP

Internal or Interior, learn the routers of EBGP within the AS. 

Helps solve issues regarding **scalability** when EBGP learns a large amount of routers. Can be solved with IBGP, which will redistribute all the routers learned via eBGP.

BGP internally, can provide flexible tools to implement custom routing policies within the AS itself. Additionally, it is highly configurable, allowing control over what routers are advertised and received.

By sharing eBGP routes internally, peers are opened to use you as a transit 

**Message Types** are the same as eBGP.

Difference is that IBGP cannot advertise learned prefixes for eBGP to another IBGP neighbor, as the same **AS-Path** can cause looping. IBGP routers need to be fully connected to learn routes of each other.

## Failure Handling

If a pair of routers within the AS using IBGP goes down, the BGP session will continue as one of the routers can use an indirect path through a directly connected IBGP routers in the AS.

If IBGP is connected through loopback interfaces, the BGP session will keep itself alive and reroute traffic through a link that is not down.

# BGP Messaging Types