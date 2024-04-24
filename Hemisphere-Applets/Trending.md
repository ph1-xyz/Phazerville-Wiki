#dualInput/inCVs #dualOutput #generator/CV 

Trending is a dual slope detector with assignable outputs.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Inputs: CV 1 and CV 2 are the incoming signals for each channel
* Outputs: Outputs A/C and B/D are assignable, and correspond to CV 1 and CV 2 channels
* Encoder: Assigns output functions, sets Sensitivity

The following functions can be assigned to each output:

* Rising: The assigned output is a gate, which is high when the signal is rising
* Falling: The assigned output is a gate, which is high when the signal is falling
* Steady: The assigned output is a gate, which is high when the signal is steady
* Moving: The assigned output is a gate, which is high when the signal is rising or falling
* ChgState: The assigned output emits a trigger when the signal changes from one state to another (e.g., rising to steady, steady to falling, falling to rising, etc.)
* ChgValue: The assigned output emits a trigger when the signal changes its value by more than 1/4 semitone (or about .02V)

## Sensitivity

The sensitivity control can be used to fine-tune the response of the slope detector. At lower settings, the detector will respond more slowly, but will be more consistent. At higher settings, the detector will respond faster, but may change direction more erratically.