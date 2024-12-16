# Modulation

Digital signals cannot be directly transmitted in the radio medium

**Digital Modulation**: Translate digital signals into (baseband) analog signals - Also known as shift keying
* Amplitude Shift Keying (ASK)
* Frequency Shift Keying (FSK)
* Phase Shift Keying (PSK)
* Quadrature Amplitude Modulation (QAM)

**Analog Modulation**: Shift the analog signals into passband signals

## Why do we need Modulation?

1. To generate a modulated signal suited and compatible to the characteristics of the transmission channel
	1. Shift information signal to the carrier frequency
	*Information signal modulates (changes) the carrier signal*
2. Reduction of antenna size
	1. Since the size of the antenna is proportional to wavelength, we want to move the information signal to a higher frequency for smaller devices.

# Demodulation

Given a transmitted signal, we can recover the original signal through demodulation.

## Course of Action

From Digital Data to Translated baseband signal
**Digital data (101101001)** -> [Digital Modulation] -> **Analog baseband signal** + **Radio carrier wave** THROUGH **analog modulation** = Shifted baseband signal (at radio transmitter)

From translated baseband signal to digital data
**Transmitted signal** -> **[Digital demodulation]** + **radio carrier wave** -> Analog baseband signal -> [**Synchronization decision**] -> **Digital data** (at radio receiver)

*Modulation is the superposition of a low-freq. signal on a high-freq. carrier wave i.e. baseband signal is translated (shifted) from low freq. to high freq.*

# Digital Modulation

* Amplitude Shift Keying (ASK):
	* One binary digit represented by presence of carrier, at constant amplitude, other binary digit represented by absence of carrier.
	* **Easy to implement, low bandwidth requirement**
* Frequency Shift Keying (FSK):
	* Information data controls the freq. of the carrier
	* **Requires larger bandwidth**
* Phase Shift Keying (PSK):
	* Information data controls the phase of the carrier 
	* **more complex**
![[ASK, FSK, PSK.png]]

# Binary Phase Shift Keying (BPSK)

Most basic form of Phase Shift Keying 
Each symbol represents 1 bit

Phase is shown as an angle and amplitude as distance from the origin

In PSK the amplitude is constant, all points lie on one circle.

```
Relationship between number of available symbols (M), and the number of bits that can be represented by a symbol (n), is: M = 2^n
```

# Quadrature Phase Shift Keying (QPSK)

Each symbol represents two bits.
4 phase shifts are used

```
Increasing the number of bits a symbol can represent, means that a higher data rates can be achieved.
```

# Higher Order PSK

We can keep increasing the number of states.
Example. 8PSK has 8 possible states.
	8 states means each symbol consists of 3 bits ($2^3=8$)

Higher order PSK (16PSK, ...) is possible, but less common.
	16 states means each symbol consist of 4 bits ($2^4=16$)

If higher data rates are needed, more complex modulation (ex. QAM) is used.

# Quadrature Amplitude Modulation (QAM)

Combines amplitude and phase modulation.

Example: 16-QAM (4 bits = 1 symbol)
	$16 = 2^4, n=4$
	Symbols 0011 and 0001 have the same phase $\phi$, but different amplitude $a$.
	Symbols 0000 and 1000 have different phase, but same amplitude

Bit error rate increases with $n$


# Which Modulation to Choose?

* Moving from BPSK -> 64QAM, increases data rate
	* Works for users that are close to the sender
