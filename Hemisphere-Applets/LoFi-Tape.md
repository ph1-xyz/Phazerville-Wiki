#generator/audio #secondaryOut/trig/EOC #dualInput/inTrigs/asGates #dualInput/inCVs/asAudio


https://youtu.be/p1SUj-F7i28

LoFi Tape is an audio-rate looper for audio or CV.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Both digital ins expect a gate signal. Digital 1 pauses playback while the gate is high. Digital 2 records from CV 1 while the gate is high.
* CV Ins: CV 1 is the signal, which can be an audio or CV signal. CV 2 is Sound-On-Sound, or the balance between the incoming signal and the looped signal.
* Outputs: A/C is the main output, and B/D is an end-of-cycle trigger
* Encoder Push: Resets the buffer and records one complete buffer cycle (about 1 second)
* Encoder Turn: Sets the end point of the buffer

LoFi Tape records at a sampling rate of 2kHz for about one second. Incoming signals are down sampled to 8 bits of resolution.