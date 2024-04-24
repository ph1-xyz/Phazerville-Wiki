#MIDI

https://youtu.be/cVnJ3RqdbJU

MIDI Out is a monophonic CV-to-MIDI interface that uses the USB port on the back of the Ornament and Crime module. The MIDI interface will appear in your computer as "Hemisphere".

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Digital 1 is a gate. A new gate causes MIDI Out to send a new Note On message, with the note based on CV 1
* CV Ins: CV 1 will be quantized to a MIDI note number, which will be sent when Digital 1 goes high. CV 2 is assignable.
* Encoder Push: Toggles the cursor between MIDI Out channel, CV 2 function, transposition, and legato
* Encoder Turn: Set channel, function, transposition, or legato

The CV 2 input may be assigned to one of the following MIDI messages:

* **Mod**: Incoming CV will be converted to a CC#1 (modulation wheel) coarse value message
* **Aft**: Incoming CV will be converted to an aftertouch message
* **Bend**: Incoming CV will be converted a pitch bend message. Pitch bend can be positive or negative, so MIDI Out expects a bi-polar voltage
* **Veloc**: Incoming CV will be used to set the velocity value of outgoing Note On messages. If Veloc is not assigned to CV 2, Note On messages will have velocity of 100.

## Transposition

Transposition has a range of -24 to +24 semitones, and this number is simply added to the computed note number.

## Legato

When Legato is Off, a Note On message is only sent when the gate goes from low to high. In other words, one note needs to be released before the next note can be sent. This option is useful for playing MIDI Out with sequencers, or when using things like LFOs for pitch.

When Legato is On, once the gate goes high, a Note On message is sent. If the note changes, then a Note Off message is sent for the previous note, and a new Note On message is sent for the new note. This option is useful for playing MIDI Out with a CV controller (Tetrapad, Pressure Points, KeyStep, etc.).

## Notes

Note 1: There is a ~3 millisecond delay between the time the gate goes high and the note value is read from CV 1. This is because Ornament and Crime has some latency in the ADCs which causes the digital inputs to register first; so some delay is required to give us the best chance of getting the right note.

Note 2: Unlike MIDI In, MIDI Out can be used in pairs.