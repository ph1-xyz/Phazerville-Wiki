#generator/CV/quantized #generator/CV/sampler #CH2/gate

Squanch is a pitch-shifting quantizer with a single input and two pitch-shifted outputs. It can be used as a voltage adder.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: A clock pulse at Digital 1 causes Squanch to sample the signal at CV 1 and quantize it. A gate at Digital 2 adds one octave to the output at A/C.
* CV Ins: CV 1 is the signal to be quantized. CV 2 is a bi-polar shift input that adds (or subtracts, if negative) voltage to or from the output at B/D.
* CV Outs: Quantized output, pitch-shifted as noted above
* Encoder: Set shift for each output, or scale

Each channel begins in continuous operation. That is, the incoming CV is quantized at a rate of about 16667 times per second. This might result in undesirable slippage between notes, so clocked operation is available.

To enter clocked operation, send a clock signal to Digital 1. A clock icon will appear next to the selector for the scale to indicate that that quantizer is in clocked mode.

To return to continuous operation, stop sending clock to the quantizer, and then change the scale. As long as no additional clock signals are received, the quantizer will remain in continuous operation.

Squanch is in Hemisphere Suite starting with v1.5.