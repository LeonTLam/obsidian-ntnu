*Adapting the modulation, coding and other signal parameters to the conditions on the radio link*

* Process is dynamic, requires some channel state information at the transmitter (**monitoring and measuring**)
* Transmitter and receiver **coordinate changes**

The goal of AMC is efficient utilization of resources through:
* Enhanced throughput
* Ability for systems to overcome fading and interference

In case of a **good-quality** channel, we choose modulation and coding combination that gives a high throughput

When conditions change, sender switches to a different modulation-coding combination.

# AMC - Challenges

If the channel changes faster than expected, AMC will perform poorly. AMC will not be able to adapt quickly to the quality of the channel.

Error in the channel estimate will result in wrong choice of data rate and coding for error correction.

AMC requires high complexity
