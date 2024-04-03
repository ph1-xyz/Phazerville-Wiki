Scope is a simple CV and clock monitoring tool.

Controls
* Digital Ins: Digital 1 is a clock for the BPM display. Digital 2 determines the wavelength for the visual display of CV 1 data (as of Hemisphere Suite 1.1)
* CV Ins: CV 1 goes to the scope, and CV 2 goes to the numeric CV monitor
* CV Outs: A/C passes CV 1 and B/D passes CV 2
* Encoder Push: Freezes and unfreezes scope and CV monitor. BPM will continue to function
* Encoder Turn: Sample rate

The value of the CV monitor is a direct reflection of the O_C's pitch value. It isn't a measurement in any particular units, but 5 volts will be around 7700 or so.

The "sample rate" shown when the encoder is turned is the number of 60µs "ticks" that will elapse between samples. 64 samples will be shown on the display at any time. The display is bi-polar. You can use the encoder to find the best rate at which to view a waveform. _Starting at Hemisphere Suite 1.1: If you send a clock to Digital 2 with the same period as the signal to CV 1 (for example, EOR trigger of Maths while viewing a waveform from Maths), Scope is automatically adjust the sample rate for the best view._

_Note: Everything's approximate, including the CV passthru._