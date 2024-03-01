AD EG is an attack/decay envelope generator with forward and reverse trigger inputs, and end-of-cycle trigger output.

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Triggers the AD envelope   | Triggers the envelope in reverse (DA) |
| CV In          | Attack modulation (bipolar) |      Decay modulation (bipolar)       |
| Output         |          Envelope           |         End of Cycle trigger          |

Note that triggering the envelope in reverse does not change the CV modulation controls, meaning that CV 1 controls the effective "attack" segment regardless of direction.

### UI Parameters
* Attack duration
* Decay Duration 


Adapted from [AD EG](https://github.com/Chysn/O_C-HemisphereSuite/wiki/AD-EG) © 2018-2022, Jason Justian and Beige Maze Laboratories. 