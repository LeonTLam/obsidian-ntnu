Figure 1, high level view of generic router architecture. Four router components can be identified.
![[Router architecture.png]]
### Inside a Router Architecture

- **Router Components**:
    - **Input Ports**:
        - Terminates incoming physical links.
        - Performs **link-layer functions** for interoperability ([[Network Layers]]).
        - Executes **lookup function** to decide on the output port via **forwarding table**.
        - Routes control packets to the **routing processor**.
    - **Switching Fabric**:
        - Links input ports to output ports; operates within the router.
        - Routes packets internally from inputs to designated outputs.
    - **Output Ports**:
        - Holds and transmits packets onto outgoing links.
        - Performs necessary link-layer and physical-layer tasks.
    - **Routing Processor**:
        - Manages control-plane functions.
        - Executes **routing protocols**, maintains **routing tables**.
        - Communicates with **SDN controllers** for routing table entries.
        - Oversees **network management**.

### Input Port Processing & Forwarding

- [[Forwarding Table]]: Maps destination addresses to output ports.
- **Longest Prefix Matching**:
    - Uses longest address match to decide the output port.
- **High-Speed Lookup**:
    - Uses **TCAM** for fast address lookup; e.g., Cisco 6500 & 7600 series handle millions of entries.
- **Input Queueing**:
    - Queues packets if switching fabric is overloaded.
    - **Head-of-the-Line (HOL) Blocking**: Front packet in queue blocks others if destined for a busy output.

### Switching Fabric Techniques

1. **Switching via Memory**:
    - Traditional; CPU-controlled packet routing.
    - Slow; bandwidth limitations on reading/writing memory.
2. **Switching via Bus**:
    - Shared bus connects input and output ports; each packet pre-pends label for destination port.
    - Limited by bus speed; suited for **small networks**.
3. **Switching via Crossbar Interconnection Network**:
    - Parallel connections allow simultaneous data transfers.
    - Non-blocking design; used in **Cisco 12000 series**.
([[Switching Mechanism]])
### Output Port Processing & Queuing

- **Output Queueing**:
    - Occurs when multiple packets target the same output port.
    - Causes packet loss if memory for queued packets is exhausted.
- **Active Queue Management (AQM)**:
    - **Random Early Detection (RED)**: Proactively drops packets to signal congestion.

### Packet Scheduling Techniques

1. **First-In-First-Out (FIFO)**:
    - Transmits packets in arrival order.
2. **Priority Queuing**:
    - Assigns priority levels; transmits highest priority first.
    - E.g., network management packets > user traffic.
3. **Round Robin**:
    - Alternates transmission among classes, following circular order.
4. **Weighted Fair Queuing (WFQ)**:
    - Assigns weights to classes for **bandwidth allocation**.
    - Ensures proportional bandwidth for each class based on weight.