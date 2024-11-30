- **Purpose**:
    - Determines the **output port** to forward each incoming packet based on destination address.
- **Structure**:
    - Entries typically include **prefixes** representing destination address ranges and associated output ports.
- **Longest Prefix Matching**:
    - The router uses the **longest match rule** to resolve conflicts when multiple entries match the destination address.
    - Example: If an address matches both 24-bit and 21-bit prefixes, the router selects the 24-bit prefix as it’s the longest match.
- **Efficiency Techniques**:
    - **TCAM (Ternary Content Addressable Memory)**:
        - Specialized hardware for rapid lookups.
        - Enables near-instantaneous address matching, essential for high-speed routers.
        - Used in devices like **Cisco Catalyst 6500 & 7600 Series** for massive, high-speed forwarding tables.
    - **On-Chip Memory and DRAM**:
        - **SRAM** (as a cache for **DRAM**) allows faster access for high-speed forwarding tasks.

Hosts do not have complete knowledge of all possible destination addresses. Most hosts have only two entries in their forwarding table:

* An entry for the local network
* Default entry for a directly-connected router

The host sends all nonlocal datagrams to the local router for delivery. 
A host can forwards datagrams successfully even if it only has partial forwarding information because it can rely on a router.

```Example
In a star-shaped topology, it would become an ussie when the central intersection fails because no equipment is fast enough to serve as a central switch which all traffic passes.

Having all information on all possible destinations in all routers is impractical because it will require large voluems of information to be changed, when a new change occurs in the system.
```

Therefore, we seek a solution that allows groups to manage local routers autonomously, adding new network interconnections and routes without changing the forwarding information in distant routers.