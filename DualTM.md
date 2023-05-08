Adapted from the original [**ShiftReg**](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Shift-Register-(formerly-Turing)) applet, this pair of 32-bit shift registers is designed to be the ultimate source of generative sequences. Digital inputs 1 & 2 are still _Clock_ & _p-gate_, respectively. The CV inputs and outputs are assignable.

The **Slew** parameter allows extreme smoothing on the output stage for portamento and gentle modulation. It acts as a Decay tail on the Trigger output modes. With CV input modulation of Slew, you can modulate the smoothing - CV control over decay envelopes, or variable portamento.

## Output Modes

* Pitch 1 - derived from 8 bits of the FIRST register
* Pitch 2 - derived from 8 bits of the SECOND register
* Pitch 1+2 - derived from the average of the two registers, optionally crossfaded via CV
  - in 1.5.x, it was actually the SUM of the two pitches; changed in v1.6
* Mod 1 - unquantized bipolar modulation from FIRST register
* Mod 2 - unquantized bipolar modulation from SECOND register
* Trigger 1 - output trigger pulse when current bit is 1 on the FIRST register
* Trigger 2 - output trigger pulse when current bit is 1 on the SECOND register
* Gate 1 - hold high if current bit is 1 on FIRST register
* Gate 2 - hold high if current bit is 1 on SECOND register
* Gate 1+2 - two-level gate output from the sum of the current bits

## Input Modes

* Slew - bipolar modulation of the Slew amount
* Length - bipolar modulation of the pattern length
* p - bipolar modulation of probability
* Range - bipolar modulation of Range
* Transpose 1 - offset Pitch 1 (basic voltage adder)
* Transpose 2 - offset Pitch 2
* Crossfade 1+2 - Affects the combo Pitch 1+2 Output mode
  - at 0V or unpatched, the two pitches are averaged
  - Positive voltage fades toward Pitch 2; negative voltage toward Pitch 1 (i think, lol, somebody should check my math)
