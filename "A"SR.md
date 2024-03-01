"A"SR is an "Analog" Shift Register simulation with a 256-step ring buffer. When selected in one hemisphere (Unlinked Mode), it has two indexed outputs. When selected in both hemispheres (Linked Mode), the same buffer is used across all four outputs and a link icon will appear in the upper right corner of the screen.

### I/O (Unlinked Mode)

|                |              1/3            |                   2/4                                    |
| -------------- |:---------------------------:|:--------------------------------------------------------:|
| Trig (Digital) | Clock (Advance buffer)      | Freeze writing buffer (Gate)                             |
| CV In          | Signal to be sampled        | Index (n) modulation (bipolar between -32 and 32 steps)  |
| Output         | Most recent value in buffer | Buffer value n steps in the past                         |

### I/O (Linked Mode)
When linked, the scale may be different for each hemisphere, but the base index will be the same.

|                |              1              |                   2                                      | 3 | 4 |
| -------------- |:---------------------------:|:--------------------------------------------------------:|:------:|:-------|
| Trig (Digital) | Clock (Advance buffer)      | No effect                            | No effect | No effect |
| CV In          | Signal to be sampled        | Index (n) modulation   | No effect | Index (m) modulation)
| Output         | n steps  |                       |

Note: At an index of 0, all outputs will be the same. When the index value is modulated by CV, a small CV indicator displays below the value.


Linked Operation

When linked, the scale may be different for each hemisphere, but the base index will be the same. Digital 1, Digital 2, and CV 1 do nothing. The index for each side may be modulated independently using CV 2. When the index value is modulated by CV, a small CV indicator displays below the value.

Linked outputs are routed as follows:

Out A: The most recent sample
Out B: n steps back
Out C: 2n steps back
Out D: 3n steps back
where n is the index.



### UI Parameters
* Index
* Scale


Adapted from ["A"SR](https://github.com/Chysn/O_C-HemisphereSuite/wiki/%22A%22SR) © 2018-2022, Jason Justian and Beige Maze Laboratories. 