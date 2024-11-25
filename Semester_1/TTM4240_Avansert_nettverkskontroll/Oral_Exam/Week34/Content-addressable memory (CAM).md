# What CAMs are
 * Hardware search engines
 * Much faster than algorithmic approaches
 * Composed of conventional semiconductor memory (usually SRAM)
 * Mostly used for search-intensive tasks - packet forwarding and packet classification in Internet routers

Routers forwarding incoming packets by using a address lookup function. Examine packet's destination address and chooses accordingly which outport port to send the packet.

The router's list of destination addresses and corresponding outport is called a [[routing table]].

| Line No. | Address (Binary) | Output Port |
| -------- | ---------------- | ----------- |
| 1        | 101SXX           | A           |
| 2        | 0110X            | B           |
| 3        | 011XX            | C           |
| 4        | 10011            | D           |
If the router receives a packet with incoming address **01101**, it will match both Line 2 & 3. In this case, line 2 is selected due to having the most matching defined bits, indicating the most direct route to destination. This is called longest-prefix matching and is required to implement the most recent *IP* networking standard.

