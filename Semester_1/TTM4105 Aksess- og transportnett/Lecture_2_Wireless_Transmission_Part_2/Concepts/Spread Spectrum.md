*Narrowband Signal -> can be wiped up by frequency-dependent fading*

**Approach:** Spread the narrowband signals into broadband signal using a special code

```Explanation
Communication technique that spreads a signal over a wider frequency band than necessary for transmission. Makes signal more resitant to interference, noice and eavesdropping.
```

## Process

* Input signal is encoded to a channel and modulated with a specific spreading.
* At the receiver, the signal is demodulated and according spreading captured to decode as output signal.

## Components

* Channel Encoder: Adds redundancy to data for error detection and correction
* Spreading Code Generator: Produces a pseudorandom code that spreads data signal over a wider frequency band.
* Modulator: Combines data signal with spreading code to produce spread spectrum signal

## Advantages

* Resistant to narrowband interference
* Signals become hard to detect, ensures better security
* Efficient multiplexing, can coexist with several other signals without dynamic coordination.

## Disadvantages

* Increased complexity at receiver
* Requires wide frequency band to spread signal

## Methods/Techniques

* Direct Sequence (DSSS)
* Frequency Hopping (FHSS)

# Direct Sequency Spread Spectrum (DSSS)

* Uses pseudo random chipping sequence to encode user data with **XOR** operation

| A   | B   | A XOR B |
| --- | --- | ------- |
| 0   | 0   | 0       |
| 0   | 1   | 1       |
| 1   | 0   | 1       |
| 1   | 1   | 0       |
