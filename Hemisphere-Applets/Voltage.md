#utility #dualInput #dualOutput #gate 

Voltage is a dual gate-activated fixed-voltage emitter.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Gate for each channel
* CV Outs: For each channel, outputs specified voltage or 0V, depending on gate state
* Encoder: Determine gate behavior for each channel

The voltage range is -3V to +5V, selectable in 1 semitone (approx. .08V) increments.

For output, there are two gate states available:

* **G-On**: When the gate of the corresponding digital input is high, the output is the specified voltage. Otherwise, it's 0V.
* **G-Off**: When the gate of the corresponding digital input is low, the output is the specified voltage. Otherwise, it's 0V.

The indicator over the output name (A,B,C,D) will display when the corresponding output is emitting non-zero voltage.

Voltage is available in Hemisphere Suite from v1.4.