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

**Digital data (101101001)** -> [Digital Modulation] -> **Analog baseband signal** + **Radio carrier wave** THROUGH **analog modulation** = Shifted baseband signal