#sequencer #CVgenerator #gateGenerator  #resetOnCH2 #masterClockOnCH1 #probability 

TB-3PO is a TB-303 style, pitch CV and gate pattern generator robot, capable of fixed-time, exponential slides on the pitch CV for that secret TB sauce. It will do mono-pitched style 303 lines on one end, or full-range, Turing Machine style stuff on the other, all designed and tuned for musicality and calls/responses in live wiggling.

* Video overview: https://www.youtube.com/watch?v=AHC2zWnkjJY
* Synth Dad Tutorial: https://youtu.be/m08NMHuhFnE


Controls

- Digital Ins: 1:Clock,  2:Reset / Regenerate
- CV Ins:   1:Transpose, 2:Density (Center point)
- CV Outs:  A:V/Oct CV + glide, B:Gate (3v normal, 5v Accent)
- Encoder: Sets the seed as unlocked or locked, edits unlocked seeds, sets note/pitch density, quantization scale, root note, and number of steps in the pattern.

## Seed
The seed parameter controls the random pattern generation. This is done deterministically, which means for the same seed you'll get the same patterns, based on the other controls.

### Locking and Unlocking
By default the seed is unlocked (die icon) and will randomly change on every reset input pulse. Turning the encoder to the right will lock the seed (lock icon) and prevent it from changing when reset pulses restart the pattern.

### Manual reset
When the seed die icon is selected, turning the encoder to the left once will reset the pattern after randomly choosing an entirely new seed. When the seed has the lock icon (turned right,) turning right once more will reset the pattern but leave the seed unchanged.

### Editing the seed
When the seed is locked, pressing the encoder advances to each of the four seed hex digits in turn. In this way you can experiment or return to past favorite seeds.

## Density
A bi-directional 'density' control specifies how many of the pattern's steps are likely to be gated, as well as the number of pitches that will be selected from. It ranges from -7 to +7:

### Value / Gate Count /  Pitches

- -7 / High / Root Only
- -6 / High / Root and +1 note in scale
- -5 / Med / Some notes in scale available
- ...
- -1 / Low / Most notes in scale available
-  0 / Low / All Notes in scale Available
-  3 / Med / All Notes in scale Available
- +7 / High / All Notes in scale Available

Density changes are applied on every clock, but if the seed is locked, specific values of density will give the same subset of patterns. In this way you can break down from busy to sparse and back.

### Density CV
When the cursor is on Density, it can be changed directly by turning the encoder. CV Input 2 applies offsets to this centerpoint value. CV is bipolar, with every +-2.5 volts corresponding to +-7 density steps. Due to the O&C's CV input range of approximately -3v to +6v, this means that there is an effective CV range of about -8 to +15 density values from the encoder-set center point.
Turning the encoder while nonzero CV is applied will show the encoder's value alongside a "knob" icon momentarily, so the offset can be edited precisely even while CV is modulating it.
Note that if the encoder value is set to -7 then the full range of density values is available by applying CV 0-5v.

## Scale
Sets the quantization scale to use for the pattern, and makes only those notes available to the pattern generator. It affects the current output CV immediately and applies to the pattern on the next clock.

## Root Note
Sets the root note from C to B, transposing the entire pattern. The octave can also be changed by scrolling beyond these notes. Due to space restrictions, the root note is saved but its octave is not.

## Pattern Length
Sets the length of the pattern from 1-32 steps. This doesn't alter the pattern apart from setting the loop point.

## Step Settings
Like on the TB-303, each step can have Gate, Accent, Glide, +octave or -octave set on it. TB-3PO chooses these values randomly based on the seed and some 303-like rules. Gates emulate the TB-303 by going high for 50% of the detected clock rate, unless they have slide set. In this case they stay high through the next step, when an exponential, fixed-time glide to the next step's pitch is engaged. Accent steps output the gate at 5v instead of 3v, which may be useful with a secondary VCA to punch them a bit.

## Visualization
- The heart icon will beat whenever the pattern is reset
- The seed die icon will hop whenever a new seed is randomly picked
- A CV icon next to density indicates that a +- offset is being applied to the encoder-set density value.
- A Knob icon next to density indicates that the encoder-set density value is being shown momentarily.
- A single octave keyboard shows the current playing step's pitch, quantized to semitones
- Icons to the keyboard's right:
  - "!" Indicates that the current step has an Accent and the gate cv will be 5v instead of 3v
  - A note-with-arrow icon indicates a step that has Slide active
  - A wiggly waveform icon shows that an active exponential pitch bend is occurring to reach the current step's pitch
  - UP and DOWN arrows indicate if the current step is transposed up or down by one octave, respectively

