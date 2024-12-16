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