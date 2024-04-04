#audioGenerator 

Dr. Crusher is a single-channel sample rate and bit resolution reducer for CV or audio signals.

Controls:
* Digital Ins: A gate signal to Digital 1 defeats the effect and passes the signal from Out A at maximum rate and resolution
* CV Ins: CV 1 is the signal input
* Outputs: Out A/C is the output with rate and resolution reduction applied, and Out B/D is the signal at maximum rate and resolution
* Encoder: Alternate between sample rate (.5kHz ~ 16.7kHz) and bit resolution (2-bit ~ 14-bit) selection

Note that the maximum rate (16.7kHz) and resolution (14-bit) values are the maximum values available to the firmware, so some "crushing" will always be applied, no matter what, including when the "defeat" is activated and when monitoring Out B/D.

If you're not getting any signal at lower bit resolutions, increase the input amplitude.

Dr. Crusher is in Hemisphere Suite starting with v1.7.