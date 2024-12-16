# Simplex

* Communication is unidirectional
* Only one of the two devices on a link can transmit, the other can only receive
* Entire capacity of the channel is used to send data in one direction
* I.E. Radio station

# Half-duplex

* Each station can both transmit and receive, but not at the same time
* When one device is sending, the other can only receive
* Entire capacity of channel can be utilized for each direction
* I.E. CB Radio, standard Ethernet

# Full-duplex

* Data is simultaneously transmitted and received between stations
* Typically uses two separate channels for supporting simultaneous transmission and reception by a host
* Capacity is divided between two directions
* I.E. cellular

# Duplexing

* Allows subscriber to send and receive data to/from the Base station at the same time
	* Talk and listen simult.
* **Forward channel or downlink (DL)** Base station -> user
* **Reverse channel or uplink (UL)** user -> Base station
* Two techniques
	* Frequency Division Duplexing (FDD)
	* Time Division Duplexing (TDD)

# Frequency Division Duplexing (FDD)

* Two distinct bands of freq. for each user
	* Forward band (From BS to mobile)
	* Reverse band (Mobile to BS)
* Duplexer filters out any interference between two bands
* Most c