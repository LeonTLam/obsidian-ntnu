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

# Nyquist Bandwidth

**Noiseless channel**
$$C = 2B\times \log_2 M$$
* C = bit rates (bps)
* B = Bandwidth (Hz)
* M = number of discrete signal or voltage levels to represent the data

```Example
Consider noiseless channel of 3 kHz, transmitting signal of 2 levels. Find the bit rate.
```

$$2\times 3\text{ kHz}\times \log_2 2 = 6 \text{ kHz} \times 1$$

```Example
What is the bit rate for transmitting signal of 4 levels?
```
$$2\times6 \text{ kHz }\times \log_2 4 = 6 \text{ kHz} \times 2 = 12 \text{ kbps} = 12000 \text{ bps}$$

# Wireless Channel Capacity - Shannon Formula

* Noisy Channel
$$C=B\log_2(1+\text{SNR})$$
* C = bit rates (bps)
* B = Bandwidth (Hz)
* SNR = Signal-to-noise ratio (in linear scale)

* Represents the theoretical maximum that can be achieved
	* Formula assumes white noise only (thermal noise)

```Example
Extremely noisy channel, SNR=0
C = B*log_2(1+0) = 0 -> no theoretical capacity, therefor cannot receive data.
```

```Example
Spectrum of a channel between 3 MHz and 4 MHz,
SNR_dB = 24 dB.
What is the channel capacity?
```

$$B = f_{high}-f_{low} = 4 \text{ MHz} - 3 \text{ MHz} = 1 \text{ MHz}$$
$$SNR_{dB} = 24 \text{ dB} = 10\log_{10}(\text{SNR})$$
$$C = 1 \text{ MHz}\times\log_2 (1+\text{SNR}) = $$
