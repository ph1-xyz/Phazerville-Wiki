This is a relatively straight-forward implementation of neo-Riemannian transformations for generating triad (three note chord) progressions (see the [_Credits, thanks, acknowledgements, and sources of inspiration_](#credits,-thanks,-acknowledgements,-and-sources-of-inspiration) section for more details on neo-Riemannian music theory).
### Controls

|       | Left Encoder                                                                                                                                                                  | Right Encoder                                                                                                     |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| TURN  | Root note transpose up or down                                                                                                                                                | Navigation mode: move up and down through the menu items. Edit mode: increase or decrease the value being edited. |
| PRESS | Toggle display of note numbers (semitone offsets from the root note) or names (note: the names are the simplest possible mapping, thus there are no enharmonic substitutions) | Toggle between menu navigation (selection) mode and value editing mode                                            |
| LONG  | Reset to defaults                                                                                                                                                             | App selection menu                                                                                                |

|            | Up Button                      | Down Button                    |
| ---------- | ------------------------------ | ------------------------------ |
| PRESS      | Increment chord inversion by 1 | Decrement chord inversion by 1 |
| LONG PRESS |                                |                                |

In settings mode, the top line of the display shows, from left to right:
 - the current root note for the root (initial) chord
 - the musicological mode (major or minor) for the root chord 
 - the three notes comprising the current triad being output. Clicking on the left encoder toggles between note display and display of semitone offset from the root note.

The root note can be changed using the _Transpose_ setting in the menu. The left encoder can also be used to change this setting at any time (such as during live performance). The voltage input on CV1 also changes the root note (i.e. the transposition).

The musicological mode of the root chord is set by _Root mode_ in the menu to either major or minor. Chord inversion is similarly set using the _Inversion_ menu item. The voltage input on CV4 also changes the inversion.

The pitch voltage (scalled to 1V/octave) for the root note appears on output A. The pitch voltages for the three notes of the current triad appear on outputs B, C and D. Thus, to pproduce chords, you should feed the B, C and D outputs into the 1V/octave pitch inputs of three VCOs. 

Trigger inputs TR2, TR3 and TR4 are used to apply the P, L or R transformations (see below). Trigger input TR1 resets the current triad back to the root chord.

If multiple triggers are received, the reset input (TR1) always has priority, then all triggered transforms are applied. The order in which they are applied can be set in the menu by the _Priority_ setting.

The neo-Riemannian transformations themselves are quite simple, and "reversible" i.e. applying them twice returns the original triad. The following basic tranformations are used:

- P (Parallel): Moves the third up or down a semitone, thus P(Cmaj) = Cmin, P(Cmin) = Cmaj.
- L (Leittonwechsel): Converts a major triad to a minor by shifting the root down a semitone and making the third the root, or from minor to major by moving the fifth up a semitone to become the root.
- R (Relativ): Converts a major triad to its relative minor, or a minor triad to its relative major.

Internally, the triad is stored in a neutral form (basically just offsets), thus the chord voicing is preserved and can be shifted easily to the quantised root note, and inversions created on-the-fly. For an alternate way of implementing these transformations, see the documentation of the [Tonnetz Sequent](http://www.noiseengineering.us/tonnetz-sequent/).

A brief video illustrating the operational principles of the _Harrington 1200_ app is [available on YouTube](https://www.youtube.com/watch?v=sbaN6Xytl7o).

### Screensaver display

The current triad (output as pitch CVs on the B, C and D sockets) is shown graphically on the left. The circumference of the circle has 12 points on it, one point for each semitone in an octave, with C at the 12 o'clock position. The current triad is indicated by the three dots, joined to form a triangle. The middle section of the screensaver display shows the last four transformations applied, with the most recent one at the top. The rightmost section indicated the current triad being output, with numbers showing the octave for each note.

Tip: for a pretty display, patch the output of an LFO into CV1 in order to rapidly rotate the root note up and down.
 
### Settings
|Setting|Meaning|
|---|---|
|`Transpose`|Shift root/triad in semitones (can be offset by CV1)|
|`Root mode`|Mode of root triad, either `maj` or `min`|
|`Inversion`|Chord inversion (can be offset by CV4)|
|`Priority`|Order in which transforms are applied if multiple triggers on TR@, TR3 and TR4 are received simultaneously|
|`Output mode`|Output mode, with the default being `chord`, or use `tune` to output the quantised root on all four output channels|

### Inputs and outputs



|     | 1                                                      | 2                                             | 3                                                         | 4                                             |
| --- | ------------------------------------------------------ | --------------------------------------------- | --------------------------------------------------------- | --------------------------------------------- |
| TR  | Reset to root triad                                    | P transform                                   | L transform                                               | R transform                                   |
| CV  | Root note transposition, quantised to +/- 24 semitones | Octave transposition                          | Post-transformation transposition, quantised to semitones | Chord inversion                               |
| OUT | Quantised root                                         | Transformed & inverted triad (also quantised) | Transformed & inverted triad (also quantised)             | Transformed & inverted triad (also quantised) |

### Tips

Try using a rhythm generator, such as the Mutable Instruments [Grids](http://mutable-instruments.net/modules/grids) module, or the ALM/Busy Circuits [Pamela's Workout](http://busycircuits.com/alm001/) module, or the Rebel Technology [Stoicheia](http://www.rebeltech.org/products/stoicheia/) module, or some combination of clock division and logic modules, or even a second O+C module running the _Piqued_ app with Euclidean trigger filters engaged, to trigger the P, L and R transformations (via trigger inputs TR2, TR3 and TR4) in varying patterns to create a variety of chord progressions that may or may not be musically pleasing, or interesting, or horrifying.

### Possible future enhancements 

 - Provide an option which outputs the sum, or other linear combinations, of the pitch CVs for the current triad, on output A, instead of the pitch CV for the root note. No idea if that would be musically useful or not, but it can't hurt to try.

 - add Euclidean trigger/clock filters to the Harrington 1200, so that a single clock input can create a polyrhythmic pattern of triggers to drive the transformations.

 - work out to what use the CV2 and CV3 inputs might be put (maybe for the Euclidean trigger filter mentioned above?)

 - portamento for chord transitions, which may or may not be useful for chords (it is not traditional)

### Example tracks

  - [La Petite Souris](https://soundcloud.com/bennelong-bicyclist/harrington-1200-petite-souris) - composed live, in one take, entirely by the _Harrington 1200_ app, driven by a Mutable Instruments Grids module.
  - [Deus ex macchiato](https://soundcloud.com/bennelong-bicyclist/deus-ex-macchiato) - another track composed on-the-fly entirely by the _Harrington 1200_ app.