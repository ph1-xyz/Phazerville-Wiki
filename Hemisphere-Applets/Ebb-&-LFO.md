#audioGenerator #LFO #resetOnCH2 #syncable 

This is a single Tides-like oscillator. Both inputs and outputs are configurable. The outputs are visualized on the screen.

It can function like a looping envelope generator or an audio-rate oscillator, with modulatable parameters for morphing the contour.

### Digital Inputs
* Clock Sync
* Reset

### CV Inputs
These are also the corresponding on-screen parameters.
Each input is assigned to one of:
* Frequency (**Hz**) - tracks V/Oct for audio-rate operation
* **Sl**ope - skews the waveform (much like the [SkewedLFO](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Skewed-LFO) applet)
* **Sh**ape - morphs between various curved segment combos
* **Fo**ld - wavefolder!

### Outputs
Each output can be one of:
* **Un**ipolar
* **Bi**polar
* Gate **Hi**gh - starts low, goes high at the end of the Attack phase
* Gate **Lo**w - starts high, goes low at the end of the Attack phase

# Credits
The original applet and backend _tideslite_ algorithm were written by **qiemem** (Bryan Head)