Open systems interconnection (OSI) model, enables diverse communication systems to communicate using standard protocols. Can be seen as a universal language for computer networking, based on splitting up a com. system into seven abstract layers.

1. Physical Layer (Lowest layer)
		Physical equipment involved in data transfer (cables and switches). The layer where data gets converted into a bit stream (1s and 0s). 
2. Data Link Layer
		Facilitates data transfer between two devices on the same network. Takes packets from the network layer and breaks them into smaller pieces called frames. Layer is also responsible for flow control and error control in intra-network communications.
3. Network Layer
		Responsible for facilitating data transfer between two different networks.. If two devices communicating are on the same network, the network layer is unnecessary. Network layer breaks up segments from the transport layer into packets, on the sender's device, and reassembles these packets on the receiving device. This layer also finds best physical path for data to reach its destination.