#masterClockOnCH1 #dualTriggerInput

_Palimpsest_ is an accent sequencer that composes a pattern by way of a repeated sequence of trigger impressions.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Clock to Digital 1 advances the sequence step. Digital 2 is the "Brush" input.
* CV Ins: CV 1 modulates Decompose, and CV 2 modulates Compose
* CV Outs: A/C is the accent output, and B/D is a trigger output sent when the level of the composed step is around 3V
* Encoder Push: Moves cursor between Compose, Decompose, and Length settings

_Palimpsest_ for Ornament and Crime is a port of this developer's alternate firmware for Mutable Instruments Peaks.

The idea behind Palimpsest is to write sequences gradually, using a pair of trigger signals. One of the triggers (Digital 1) clocks the sequencer. The other trigger (Digital 2) is a "Brush," which adds a CV value ("Compose") to the current step. If the sequencer is clocked without a brush trigger having arrived during that step, a CV value ("Decompose") is _subtracted_ from that step.

The results can be subtle, with a small Compose value and small or zero Decompose value. Or more dramatic shifts can be made, with larger values.

The sequence length can be between 2 and 16 steps. _When the cursor is on the Length setting, the sequence is locked, and incoming triggers will not affect it._