#generator/CV/quantized #singleOutput #CH1/trig/mainClock #CH2/gate 

Scale Duet is a single-channel quantizer that allows you to switch between two user-defined scales. The scales are edited with an on-screen keyboard.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls:
* Digital Ins: Digital 1 clocks the quantizer, and Digital 2 is a gate that chooses between Scale 1 (low) and Scale 2 (high)
* CV Ins: CV 1 is the signal to be quantized.
* Outputs: A/C is the quantized output for the selected scale
* Encoder Push: Toggles the note above the cursor ON or OFF. A small square will appear on the keyboard for notes that will be played when that scale is selected.
* Encoder Turn: Moves through the notes for each scale, and between Scales 1 and 2.

Scale Duet differs from Dual Quantizer in a few important ways:

* Scale Duet plays from two user-defined scales, rather than pre-programmed scales
* It quantizes only one value at a time
* It does not have a continuous mode; it only quantizes when clocked