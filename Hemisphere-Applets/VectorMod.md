#generator/envelope  #dualInput/inTrigs/asTrigs #dualInput/inCVs/asGates #dualOutput/CVs  #dualChannels 

VectorMod is a dual triggered one-shot or cycling modulation source based on Vector Oscillator waveforms. There is a variety of built-in waveforms from which to choose, or you can create your own with the [Waveform Editor](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Waveform-Editor).

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: A trigger at each input starts the corresponding Modulator
* CV Ins: A high signal (gate) at each input causes the corresponding Modulator to cycle
* Outputs: Output A/C is bi-polar the signal for Mod 1, and Output B/D is the bi-polar signal for Mod 2
* Encoders: Push to alternate the cursor between Mod 1 frequency, Mod 1 waveform select, Mod 2 frequency and Mod 2 waveform select

The speed of the Modulator is determined with a single frequency control. The higher the frequency, the faster the Modulator will run.

VectorMod is in Hemisphere Suite starting with v1.6.