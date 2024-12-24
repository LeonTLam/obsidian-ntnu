A **STUN SERVER** provides devices behind firewalls and NATs ways to discover public IP addresses and open communication channels. Making it easier for devices to communicate with each other across the internet.

[[Network Address Translation (NAT)]]is used to allow multiple devices to share a single public IP address. However this can cause problems for real-time communication protocols like **Voice over Internet Protocol** (VoIP), because the NAT device modifies the IP address and port number of the client.

When a client tries to establish a connection, it sends a request to the STUN server, the STUN servers responds with the client's public IP address and port number, allowing direct connection with other clients.