Errors must be detected and corrected in order to have a reliable communication

**3 common error detection techniques**:
* Parity Check
* Checksum
* Cyclic Redundancy Check (CRC)

# Parity Checks

* Parity bit(s) generated for even number of specific bit

* Checking function at receiver accepts or rejects if total number of specific bit is an even number.

## PC - Single Bit Parity

Detects single-bit error
Detects burst errors if the number of errors is odd

## PC - Two-dimensional Bit Parity

Detect and correct single-bit errors

If two bits in one data unit are damaged and two bits in the same exact position in another unit are corrupted, errors will not be detected.

# Checksum

Addition of a data segment content

* Sender: **Checksum creation**
	* Calculate checksum of data and adds to checksum field
* Receiver **Checksum validation**
	* Computes checksum of received segment
	* If computed = checksum field value, accepted
	* Otherwise, rejected

Data unit is divided into n-bit segments.
All segments are added, then the 1's complement is found with the first segment.

At the receiver, the sum of data plus checksum is performed. 
If all 1's, data is accepted

## Checksum - Disadvantage

If bits in same position but with opposite values are changed through transmission, sum will not change and receiver will not detect errors.

# Cyclic Redundancy Check (CRC)

Error detection method based on binary division

Divisor known for both sender and receiver

CRC is generated at sender and verified at receiver

* Sender performs binary division of augmented dataword and appends a remainder

* Receiver divides received data by the divisor, if result of division is all 0's at remainder, no transmission error

# Error Detection

* Generally does not provide any way to locate/correct errors

* Parity Check
	* Extremely simple, can be fooled by certain types of errors (two bits in error)
	* Useful for small frame sizes (where typical error is single bit)
* Checksum
	* Simple
	* More powerful than parity check (lower prob. of undetected errors)
* CRC
	* Most complicated and most powerful (Extremely low prob. of undetected errors for longer CRC checks)
	* IEEE 802 specifies a CRC-32 check

# Error Correction

* Error correction in two ways (may):
	* Request re-transmit of entire information (**Backward Error Correction**)
	* Receiver applies error-correction algorithms (**Forward Error Correction**)

* Problems with re-transmission
	* Not suitable for multimedia transmission
	* Not available at non bi-directional links (HDTV)
	* Reoccurring at link with high bit error rate
	* Bad QOS at a link with high latency (satellite)

# Forward Error Correction (FEC)

**Advantages**
* Saves bandwidth required for retransmission
* Does not require handshaking between source and destination
**Limitations**
* Too many errors requires frames to be retransmitted

## FEC - Codebook

* Codebook is a mapping from k-bit data sequences to n-bit codewords with n > k
* Code rate $r = \frac{k}{n}<1$
* (n,k) code

* Both transmitted and receiver know the codebook
* Transmitter takes data blocks, maps them to codewords and transmits the codeword
* Receiver receives codewords (with pot. one or more errors)a nd maps them back to data blocks

## FEC - Hamming Distance

Hamming distance between n-bit codewords v1 and v2 is defined as

$$d(v_1,v_2) = \sum^{n-1}_{l=0}XOR(v_1(l),v_2(l))$$
Simply number of bits in which v1 and v2 are different

```Example
v1 = 011011
v2 = 110001
Hamming distance d(v1,v2) = 3
```

## Redundancy vs Hamming Distance

We want hamming distance to be large and redundancy to be small

**Redundancy** = $\frac{n-k}{k}$
n - length of codeword
k - length of data block

## Minimum Distance Decoding

When an invalid codeword is received, receiver should choose valid codeword with **minimum hamming distance** to be the invalid codeword.

In the case where the lowest minimum hamming distance is the same for two codewords, and there are no other codes closer to the invalid codeword. We must conclude that the codeword cannot be decoded.