---
tags:
  - Concept
---
# Concept for [[Introduction.md]]

Process of encoding information from message source in a way suitable for transmission. Achieved by altering characteristics of a wave.

By superimposing a msg. on to a high freq. signal known as carrier wave, video, voice and other data can be transmitted.

Why modulation is needed?
* Data rate
* Antenna length
* Interference

**Input** signal can be analog or digital -> Analog & Digital modulation

**Baseband signal**, original signal that contains actual information before modulation.
* low-freq. range
* cannot efficiently be transmitted over long distances on most comm. channels.
	* requires large antennas
	* more susceptible to noise and interference

**Carrier signal**, high-freq. sinusoidal waveform used to carry the baseband signal.

$$
\begin{aligned}
c(t)=A_c \cos(2\pi f_ct+\phi)\\
A_c = amplitude\\
f_c = carrier freq\\
\phi = phase
\end{aligned}$$
* enables freq. translation
* allows multiple signals to coexist in different freq. band (multiplexing).
* better propagation through air, less attenuation and practical antenna size.

![[Pasted image 20250719101835.png]]

# Analog Modulation

Shifts the analog baseband signal into a passband signal, can be transferred on wireless medium.

# Demodulation

Extracting original information-bearing signal from a carrier wave

![[Pasted image 20250719102058.png]]