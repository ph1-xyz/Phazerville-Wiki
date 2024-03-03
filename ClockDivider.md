Clock Div is a dual, 2-stage serial clock divider and multiplier, using a single clock source. Each stage can divide from 1:1 to 1:32 (for a maximum of 1:1024), and multiply from 1:1 to 32:1 (for a theoretical maximum of 1024:1, though in practice you're unlikely to exceed 180:1 without strange behaviour). Voltage control is available for the first stage of each channel.  Complex clock divisions / multiplications made easy!

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Clock input   | Reset |
| CV In          | Div/Mult modulation Ch 1 Stage 1 (bipolar) |      Div/Mult modulation Ch 2 Stage 1 (bipolar)       |
| Output         |          Ch 1 Div/Mult result             |         Ch 2 Div/Mult result          |

Note that triggering the envelope in reverse does not change the CV modulation controls, meaning that CV 1 controls the effective "attack" segment regardless of direction.

### UI Parameters
* Ch 1 Stage 1 division/multiplication factor
* Ch 1 Stage 2 division/multiplication factor
* Ch 2 Stage 1 division/multiplication factor
* Ch 2 Stage 2 division/multiplication factor

Division works by counting clocks and sending a trigger on the _n_th clock. When the encoder is turned, the counter is reset.

Multiplication works by counting interrupt cycles (c) between the last two clock inputs, and sending a trigger every c/n cycles.

CV inputs are bipolar, with a range of about -2.5 volts to about 2.5 volts. Positive values set clock division, and negative values set clock multiplication. There's a small center detent CV range, over which range control is only set from the panel. This is done because O_C can't sense whether a jack is patched.


Adapted from [Clock-Divider-Multiplier](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Clock-Divider-Multiplier) © 2018-2022, Jason Justian and Beige Maze Laboratories. 