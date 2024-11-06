Sometimes known as the **user plane, forwarding plane, carrier plane, data path or bearer plane**.
Refers to processes responsible for **forwarding** packets from one interface to another (-- source to destination--), based on the control plane's logic.

Primary function, carry the network's user traffic (data packets) and transit the packets while applying some action to them ([[Routing tables]]).

Data planes takes packets from one port of a switch and sends them to another port through the router. Requires inpits from the control plane to determine which ports to send packets to.