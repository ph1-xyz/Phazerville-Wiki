#generator/trigger 

Burst is a burst generator based loosely on the Ladik S-075.

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Clock (optional)   | Start burst sequence |
| CV In          | Number of triggers per burst |      Spacing (bipolar)       |
| Output         |          Burst triggers           |         Burst gate (high until end of burst)          |

### UI Parameters
* Triggers per burst (1-12)
* Spacing (8ms-500ms) [Clock input overrides]
* Acceleration/deceleration (positive values space later triggers closer together)
* Randomization (humanizes trigger timing)
* Clock input multiplication/division

If Burst receives another trigger at Digital 2 before the burst sequence has finished, a new sequence will start.

When CV is received at CV 1, the Number setting at the panel is overridden. There is a center detent around 0V, so slightly more than 0V is required to change the Number.

When CV is received at CV 2, the Spacing setting at the panel is modulated. There is a center detent around 0V, so slightly more than 0V is required to change the Spacing.

Adapted from [Burst](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Burst) © 2018-2022, Jason Justian and Beige Maze Laboratories. 