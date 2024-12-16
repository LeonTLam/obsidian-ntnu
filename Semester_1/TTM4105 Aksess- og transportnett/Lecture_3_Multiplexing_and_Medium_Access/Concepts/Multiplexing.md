**Introduction to Multiplexing can be found here**
[[Semester_1/TTM4105 Aksess- og transportnett/Lecture_0_Introduction/Concepts/Multiplexing|Multiplexing Introduction]]

# Space Division Multiplexing (SDM)

* Assigns space to each comm. channel
* Guard spaces separate interference range
* Allows for reuse of same freq. at same time
* I.E. Analog TV & Radio

* SDM is implemented in cellular system with each **cell** covering a certain area.

* SDM allows **frequency reuse** if two transmitters are far enough from each other

# Frequency Division Multiplexing (FDM)

* Spectrum is divided into **smaller bands**
* Each communication channel is assigned a band
	* Does not require complex coordination
* Carrier freq. separated so signals do not overlap (**guard bands**)
* I.E. Analog TV/Radio, fiber optics (WDM)

## FDM - Disadvantages

* Inflexible
	* Some channels might need more Bandwidth than others
* Waste of BW if traffic not evenly distributed
	* Burty traffic, periods with no broadcast

# Time Division Multiplexing (TDM)

* Typical for digital systems
* Channel get the **whole spectrum** for certain amount of time
	* I.E. round-table discussions
* Used in mobile cellular systems

## TDM - Advantages

* Only one carrier in the medium at any time
* Throughput is high even for many users

## TDM - Disadvantages

* Precise synchronization is needed

# Time and Frequency Division Multiplexing

* Combines **TDM and FDM** by assigning a certain frequency band to a channel at certain time slot. I.E. Bluetooth and GSM

## TDFM - Advantage

* Protects against tapping
* Protects against frequency-selective fading 
	* Data can still be recovered using Forwarding Error Correction

## TDFM - Disadvantages

* Requires precise coordination of time and freq.
	* All devices must know the hopping pattern

# Code Division Multiplexing (CDM)

* Typical for wireless systems
* Each channel is assigned the whole spectrum
	* Each with a unique code. Bits are coded before transmission

## CDM - Advantages

* Bandwidth efficient
* No freq. coordination and synchronization needed
* Good protection against interference and tapping

## CDM - Disadvantages

* More complex signal regeneration
* Power control required

# Orthogonal FDM (OFDM)

* System bandwidth is divided into set of overlapping yet orthogonal sub-bands (subcarriers)

* Also known as multicarrier modulation
* Data is distributed over multiple carriers at precise freq.



