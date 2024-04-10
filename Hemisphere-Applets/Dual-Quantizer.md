#generator/CV/quantized #generator/CV/sampler #dualInput/inTrigs #dualInput/inCVs #dualOutput/CVs 

Dual Quantizer converts 2 independent CV inputs to pitches of specific musical scales. Clocked (sample & hold) operation is available for each channel.

See it in action: https://youtu.be/GkV-rB4ntho

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Ch 1 Clock   | Ch 2 Clock |
| CV In          | Ch 1 Unquantized CV |     Ch 2 Unquantized CV       |
| Output         |          Ch 1 Quantized CV           |        Ch 2 Quantized CV          |

Note: Each channel begins in continuous operation. That is, the incoming CV is quantized at a rate of about 16667 times per second. This might result in undesirable slippage between notes, so clocked operation is available on a per-channel basis.

To enter clocked operation, send a clock signal to a digital input. A clock icon will appear next to the selector for the corresponding channel to indicate that that quantizer is in clocked mode. 

To return to continuous operation, stop sending clock to the channel, and then change the scale. As long as no additional clock signals are received at the channel, the quantizer will remain in continuous operation.

### UI Parameters
* Ch 1 Scale
* Ch 1 Root
* Ch 2 Scale
* Ch 2 Root

Adapted from [Dual Quantizer](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Dual-Quantizer) © 2018-2022, Jason Justian and Beige Maze Laboratories. 