#masterClockOnCH1 #gateOnCH2  

RunglBook is a chaotic shift-register modulation based on Rob Hordijk's rungler circuit.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Digital 1 is the clock, and Digital 2 freezes the shift register to writing
* CV Ins: CV 1 is the signal
* CV Outs: A/C is the Rungle output based on the low three bits, and B/D is the Rungle output based on the high three bits
* Encoder: Set threshold in semitone increments

When Digital 1 is clocked, the register is shifted one bit to the left, and the signal is read. If the signal exceeds the voltage threshold, bit low bit of the shift register is set to 1. Otherwise, it is set to 0.

If Digital 2 is receiving a gate at the time the clock is received, the register is shifted, but no read is done; instead, the high bit is moved to bit 0.

Three bits of the eight-bit register are scaled to 8 possible values between 0V and 5V, and sent to the outputs. These are the Rungle outputs.

RunglBook is in Hemisphere Suite starting with v1.5.