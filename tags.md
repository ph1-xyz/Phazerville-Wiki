### I/O
#dualOutput : Produce the same kind of function (trigger, CVs or audio) over the two OUT channels.

#dualInput: Accepts two same kind (trigger or CVs) of inputs in IN channels.

#dualChannels: App has two parallel channels, performing the same function.
### Clock and Gates
#CH1/trig/mainClock : Clock on CH1/3 advances the state the applet (trigger- or CV-sequencers).

#CH2/gate : Gate on CH2/4 applies a special particular behaviour; ex.: *freezes* a sequencer, *holds* a value on an LFO.

#CH2/trig/reset : Trigger on CH2/4 applies a particular behaviour; ex. *resets* the sequencer or an LFO.
### CVs
#generator/CV/sequencer: 

#generator/CV/quantized : Applet produces, or can produce, quantized pitches.

Types ???? 
#logic: compares
#aleatoric : deals with probability


To review:
- is #dualChannels useful, compared to #dualInput and #dualOutput ?
- should #generator/CV/quantized named better? Thing to capture is musical scale; not probably just quantization of outputs which some applets do without the user asking or being able to change.
- is #logic tag useful?
