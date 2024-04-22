#envelopeGenerator #triggerable #gate #dualInput #dualOutput #independentChannels 

VectorEG is a dual envelope generator based on Vector Oscillator waveforms. There is a variety of built-in waveforms from which to choose, or you can create your own with the [Waveform Editor](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Waveform-Editor).

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: A gate at each input starts and sustains the corresponding EG.
* Outputs: Output A/C is the signal for EG 1, and Output B/D is the signal for EG 2
* Encoders: Push to alternate the cursor between EG 1 frequency, EG 1 waveform select, EG 2 frequency and EG 2 waveform select.

The EG runs freely until it gets to the second-to-last segment, and sustains at that point. When released, it proceeds to the level of the final segment at the speed specified by the final segment.

Unlike a traditional envelope generator, the speed of the envelope is determined with a single frequency control. The higher the frequency, the faster the envelope will run.

The outputs are uni-polar, and with positive offset, so that a level of -128 in the Waveform Editor corresponds to 0V, and a level of 127 is 5V.

VectorEG is in Hemisphere Suite starting with v1.6.