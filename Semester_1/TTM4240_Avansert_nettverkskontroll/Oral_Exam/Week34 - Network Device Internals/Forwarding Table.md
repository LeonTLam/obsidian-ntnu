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

Hosts do not have complete knowledge of aall possible destination addresses. M