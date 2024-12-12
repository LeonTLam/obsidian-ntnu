*Maximum rate at which data can be transmitted over a given communication path, or channel, under given conditions.*

*Data rate can be achieved is limited by impairments such as noise!*

# Concepts related to channel capacity

**Data rate** - rate at which data can be communicated (bps)

**Bandwidth** (Hertz) 
$$B = f_{high} - f_{low}$$
		It is the narrow band of frequencies that the most of the signal's energy is contained in.
		Constrained by the transmitter and the nature of the transmissions medium.

**Noise** - Average level of noise over the communications path

**Error rate** - Rate at which errors occur

# Signal Bandwidth Example

* If a signal is decomposed into 5 sine waves with frequencies of 100, 300, 500, 700, 900 Hz. What is the bandwidth of this signal?
$$B = f_{high} - f_{low}$$
$$B = 900 \text{ Hz} - 100 \text{ Hz} = 800 \text{ Hz}$$

# Signal-to-Noise Ratio (SNR)

*Ratio of the power in a signal to the power contained in the noise that's present at a particular point in the transmission
	Typically measured at the receiver*

**Signal-to-noise ratio**
$$(SNR)_{dB} = 10\log_{10}\frac{\text{signal power}}{\text{noise power}}$$
**SNR shows signal quality**
* A low SNR means low quality signal, may require further signal processing to recover original signal.