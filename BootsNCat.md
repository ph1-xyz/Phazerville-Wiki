Boots 'n Cats (BootsNCat) is a simple bass/snare drum synthesizer with stereo audio outputs.

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Bass drum trigger   | Snare drum trigger |
| CV In          | Bass drum attenuation |      Snare drum attenuation       |
| Output         |          Bass drum (or mix)           |        Snare drum (or mix)        |

Note that triggering the envelope in reverse does not change the CV modulation controls, meaning that CV 1 controls the effective "attack" segment regardless of direction.

### UI Parameters
* Bass drum tone
* Base drum decay
* Snare drum tone
* Snare drum decay
* Blend

**Tone**
* Each drum has a Tone control that sets the basic sound of the drum. For the bass drum, Tone controls the frequency, with higher values indicating a higher frequency. For the snare drum, the Tone control is more like a low-pass filter, with high values indicating a higher cutoff frequency.

**Decay**
* Each drum has a Decay control that sets the decay of the drum between about 1/10 of a second and 1 second, with higher values indicating longer decay.

**Blend**
* At a Blend level of 0, the bass drum and snare drum are totally isolated on Outputs A/C and B/D, respectively. As the Blend is increased, some of the signal from the opposite channel will be fed into each channel. A Blend level of 63 results in a 50/50 mix on both outputs.


Adapted from [BootsNCat](https://github.com/Chysn/O_C-HemisphereSuite/wiki/BootsNCat) © 2018-2022, Jason Justian and Beige Maze Laboratories. 