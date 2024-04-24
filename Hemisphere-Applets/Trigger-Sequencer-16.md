#CH1/trig/mainClock #CH2/trig/reset #generator/trigger #generator/CV/sequencer 

Trigger Sequencer 16 is a 16-step trigger sequencer. It's visually and functionally similar to Trigger Sequencer, except it's 1x16 instead of 2x8.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: A clock at Digital 1 advances the sequence. A trigger at Digital 2 resets sequence.
* CV Ins: While a gate is present at CV 1, the A/C and B/D outputs are swapped
* Outputs: A/C is the sequence's trigger output, and B/D the NOT trigger output
* Encoder Push: Cycles cursor between editing 4-step parts of the sequence and sequence length
* Encoder Turn: Adjust the selected setting

The cursor appears over four steps at a time. Turning the encoder selects a binary representation of the bit pattern. Each quarter of the sequence has sixteen possible values. That is, turning the encoder clockwise will cycle through

* (silence)
* ---X
* --X-
* --XX
* -X--
* -X-X
* -XX-
* -XXX
* X---
* X--X
* X-X-
* X-XX
* XX--
* XX-X
* XXX-
* XXXX
