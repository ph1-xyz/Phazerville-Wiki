Vector LFO is a dual low-frequency oscillator based on Vector Oscillator waveforms. There is a variety of built-in waveforms from which to choose, or you can create your own with the [Waveform Editor](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Waveform-Editor).

Controls
* Digital Ins: A trigger at each channel syncs the corresponding LFO
* CV Ins: CV 1 is bi-polar modulation of the frequency of LFO 1. CV2 is attenuation of the amount of LFO 1 that's fed into Output B/D.
* Outputs: Output A/C is the signal for LFO 1. Output B/D is the signal for LFO 2 mixed with the signal for LFO 1, with the mix based on the input to CV 2.
* Encoders: Push to alternate the cursor between LFO 1 frequency, LFO 1 waveform select, LFO 2 frequency and LFO 2 waveform select.

The LFO range is from .10Hz to 999Hz.

## Output A/C and LFO 1

Output A/C is a the output of only LFO 1. LFO 1 can be synchronized with an external clock at Digital 1, and its frequency can be modulated over a 30Hz bi-polar range with CV 1.

## Output B/D and LFO 2

Output B/D is a mixed output. By default, it is a 50%/50% mix of LFO 1 and LFO 2. Increasing voltage to CV 2 causes increasing attenuation of the LFO 1 signal. At 5V, the LFO 1 signal will be absent at Output B/D.

## Manual Oscillator Reset

When a new waveshape is selected from the panel, both LFO 1 and LFO 2 will be reset to the beginning of their respective cycles.

VectorLFO is in Hemisphere Suite starting with v1.6.