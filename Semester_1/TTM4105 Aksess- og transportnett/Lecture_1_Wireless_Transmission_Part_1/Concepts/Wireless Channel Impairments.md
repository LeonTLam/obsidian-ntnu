* Noise
	*Unwanted external signal that can impair original signal*

* Transmission Loss
	Mainly by signal attenuation (weakening of signal's strength due to noise, distance or other external factors)

* Multipath
	Caused by reflection, diffraction and scattering

* Doppler spread
	Signal distortion that is caused by the movement of mobile unit

* Methods can be used to overcome these impai:
	* Adaptive Modulation and Coding
	* Diversity Techniques
	* Data Encoding
# Attenuation

* Strength of signal falls off with distance
	* Receiving power proportional to 1/d^2 in vacuum
	* Greater at higher frequencies (Greater loss at higher frequencies)

* Received signal:
	* Must have sufficient strength so that the receiver can interpret the signal
	* Must maintain a level sufficiently higher than noise to be received without error

# Free Space Loss - Ideal Isotropic Antenna

**Free Space Loss**, ideal isotropic antenna through the following formula:

$$\frac{P_t}{P_r}=\frac{(4\pi d)^2}{\lambda ^2}=\frac{(4\pi f d)^2}{c^2}$$
* P_t = Signal power at transmitting antenna
* P_r = Signal power at receiving antenna
* lamda = carrier wavelength
* d = propagation distance between antennas
* c = speed of light (3 * 10^8 m/s)

**In dB**: 
$$L_{dB}= 10\log \frac{P_t}{P_r}$$

# Free Space Loss - Other Atennas

For other antennas, the gain of the antenna is considered:

$$\frac{P_t}{P_r}=\frac{(4\pi)^2(d)^2}{G_rG_t\lambda^2}$$
* G_t = Gain of transmitting antenna
* G_R = Gain of receiving antenna

```Definition
Antenna Gain: Power output, in a particular direction, compared to that produced in any direction by an isotropic antenna (theoritcal perfect antenna)

For isotropic antenna, gain G = 1
```

# Path Loss vs Frequency

The loss due to **frequency** increases the stronger the Hertz rate becomes, but also increases by the **distance**.

A higher **frequency** has a bigger LOSS at a longer **distance**, than a lower frequency at the same distance

# Signal Propagation

* In addition to the attenuation, the power of the received signal is also influenced by:
	* Shadowing
	* Reflection: Smooth surface > $\lambda$
	* Refraction: depending on the density of the medium
	* Scattering: Object > $\lambda$
	* Diffraction: Object with large dimensions relative to $\lambda$ and sharp irregularities (edges), causing secondary waves.

![[Signal_propagation.png]]

# Multipath Propagation

* Caused by reflection, diffraction and scaterring
* Multiple copies of the same signal may arrive at different locations (different timestamps of the signal reception)
* Intersymbol interference (ISI)
	* one or more delayed copies of a pulse may arrive at the same time as the primary pulse for a subsequent bit.

# Fading

*Deterioration of the signal quality*

* A signal out of transmitter radiates into wide direction
* Radiated signals take different paths and arrive at receiver at different timings and with different signal strength (amplitude)(multipath)
* Signal coming into receiver is the composite of all the components

## Fast Fading vs Slow Fading

* Rapid fluctuations of signal caused by movement (**Doppler Spread**)
* Time-domain
* Coherence time $T_C$ = How long a channel remains relatively constant

* If **Coherence Time $T_c$** >> bit time $T_b$ ,
	* slow fading/long term fading
* Otherwise fast fading / short term fading

```Example
Suppose a pedestrian is moving through an urban env. that has a wireless channel with a coherence time of 70 ms. The bit rate of the signal is 100 kbps. Do we have a fast fading or a slow fading
```

$$\text{Bit Time } T_b= \frac{1}{100\text{ kbps}}= 10 \micro\text{s}$$
$$T_b = \frac{1}{R_b}= \frac{1}{100 000}\text{seconds}=10\micro \text{s}$$
$$70\text{ms} >> 10\times10\micro \text{s}, \text{thus slow fading} $$

## Flat Fading vs. Frequency-Selective Fading

 **Flat Fading**, occurs when the bandwidth of the *transmitted* signal is much smaller than the coherence bandwidth of the channel.
 $$B_{signal}<<B_{coherence}$$
 This means all frequency components of the signal experience same level of fading

```Example
A transmitted signal with a bandwidth of 10 kHz transmitted through a channel with a coherence bandwidth of 150 kHz
```
* Coherent bandwidth is larger than 10x of signal bandwidth
* We have flat-fading or narrowband fading

______________________
**Frequency-Selective Fading**, occurs when the bandwidth of the transmitted signal is larger than the coherence bandwidth.
$$B_{signal}>B_{coherence}$$
Different frequency components of the signal experience different levels of fading.

```Example
A transmitted signal with a bandwidth of 1 MHz transmitted through a channel with a coherence bandwidth of 100 kHz
```
* Coherent bandwidth of 100 kHz is not larger than 10 x 1 MHz
* We have frequency-selective fading

