#MIDI

https://youtu.be/Hfowo8vF7CE

MIDI In is a monophonic MIDI-to-CV interface that uses the USB port on the back of the Ornament and Crime module. The MIDI interface will appear in your computer as "Hemisphere".

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Outputs: Assignable
* Encoder Push: Cycle cursor between MIDI channel, Out A assignment, and Out B assignment
* Encoder Turn: Change channel or assignment

Accepts MIDI data from the USB port on the back of the O_C module. If you installed Hemisphere Suite from a hex file, the MIDI driver will be called Hemisphere. If you compiled Hemisphere Suite from source, it will probably be Teensy MIDI.

The following types of MIDI data are assignable to the outputs:

* **Note#**: The output is a quantized value based on the MIDI note number
* **Trg**: The output is a trigger signal on a MIDI note on message
* **Gate**: The output is a 5 volt gate signal, starting at a note on, and ending at the corresponding note off. Since the applet is monophonic, the gate will only pay attention to one note at a time.
* **Veloc**: The output is a scaled voltage (0-5 volts) corresponding the to last note's velocity
* **Mod**: The output is a scaled voltage (0-5 volts) corresponding to the position of CC#1 (modulation wheel)
* **Aft**: The output is a scaled voltage (0-5 volts) corresponding to the aftertouch value
* **Bend**: The output is a scaled voltage (-3 to 5 volts) corresponding to the pitch bend value
* **Clock**: The output is a clock signal every twelve pulses (eight notes). The clock can be reset by turning the encoder to the right.

The screensaver for MIDI In displays the last six MIDI messages. It will always display note activity on the selected channel. Other data (note off, aftertouch, pitch bend, modulation) will only be shown if that data type is assigned to a CV output.

MIDI In is available in Hemisphere Suite.