DivSeq is a dual sequential clock divider with a single input clock. Each of the two channels is composed of a sequence of up to 5 clock dividers. Under normal operation, a step "n" triggers 1 clock pulse, skips n-1 pulses, and then steps to the next clock divider. Under CV modulation, each channel may also be in inverted mode (skip 1, trigger n-1 pulses, step), or cross-channel XOR mode. Performance mutes may be manually toggled for each divider step. Each step may be set to a divider of 0 (off) up to 63.

See it in action: https://youtu.be/J1OH-oomvMA?si=Z97wJ3HXe0HocaBa&t=357


### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Clock   | Reset |
| CV In          | Ch 1 mode modulation: inverted (positive), XOR (negative) | Ch 2 mode modulation: inverted (positive), XOR (negative) |
| Output         |          Ch 1 trigger sequence           |         Ch 2 trigger sequence           |


### UI Parameters
* Ch 1 divider value steps 1-5
* Ch 2 divider value steps 1-5
* Ch 1 performance mutes steps 1-5
* Ch 2 performance mutes steps 1-5
