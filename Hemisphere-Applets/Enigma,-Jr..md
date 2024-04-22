#quantizedPitch #CVgenerator #sequencer #probability #gateable #masterClockOnCH1 #gateOnCH2 

While Enigma imposes a track-song workflow, Enigma, Jr. allows you to organize your Turing Machines via CV. It allows playback and temporary manipulation of registers in your Enigma Register Library.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Digital 1 advances the register
* CV Ins: CV 1 is a bi-polar modulation of the pitch, and CV 2 is the Organize modulation (see below)
* CV Outs: Assignable
* Encoder: Choose Register, probability, or assign outputs

In many respects, Enigma, Jr. is similar to ShiftReg. But instead of generating a random sixteen-bit register, Enigma, Jr. uses a Register from the Enigma Register Library. Enigma may be used to shape and curate this Library (see https://github.com/Chysn/O_C-HemisphereSuite/wiki/Enigma).

Both outputs are assignable to any of the CV values that Enigma can use. These are:

* **Note**: There are five depths of note data, from 3 bits to 7 bits. At 3-bit depth, melodies will be constrained to 8 notes of the selected scale. At 4-bit depth, 16 notes; at 5-bit depth, 32 notes; at 6-bit depth, 64 notes; and, at 7-bit depth, 128 notes (or the entire MIDI note range) is available. The note types look at the least-significant bits of the current Register.
* **Modulation/Expression**: The least-significant 8 bits are used to generate a modulation value that's scaled to 0-5 volts. Modulation and Expression are identical for CV.
* **Gate**: When bit 0 is 1, the assigned output emits 5V until the next time bit 0 is 0. That is, a high gate will span multiple rotations of the Register
* **Trigger**: When bit 0 is 1, a trigger pulse is emitted at the assigned output

## Organize

CV 2 is the Organize control. When a Register has advanced to the end of its length, CV 2 is read, and a new Register is loaded, based on the CV 2 modulation. If your Library has Registers marked as Favorites, the CV will choose from among your Favorites. If you have no Favorites selected, the CV will choose at random from among all 40 Registers in the Library.

Enigma, Jr. is in Hemisphere Suite from v1.5.