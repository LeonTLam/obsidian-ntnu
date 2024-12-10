# Definition

Multiplexing is the method of carrying multiple signals on a shared medium.
- "Mux" them together at sender and "demux" them apart on receivers end
- More efficient use of transmission medium
- Sharing the medium with minimum or no interference

There are 5 dimensions to multiplexing:
* Time
* Frequency
* Code
* Space
* Polarization

# Time Division Multiplexing

```Short
A channel gets the whole spectrum for a short time
```

# Frequency Division Multiplexing

```Short
The spectrum is divided into smaller bands
```

# Types of Communication Link Sharing

## Static Multiplexing-Circuit

Each sender is given dedicated, scheduled resources according to the service agreement.
Will always have X b/s.

## Statistical Multiplexing-Packet

All users shares the resources.
Uses statistics to scale the total amount of resources needed.
Will have a variable bitrate depending on the amount of traffic the other users sends and buffer-loss

# Collision Domain

Defines set of devices on which their frames could collide. Happens in a shared network segment connected by a shared medium or using repeaters where real-time data transmissions can collide.
Results in low quality network due to delays and re-transmissions.