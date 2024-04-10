#logic #dualInput/inTrigs/asGates #CH1/CV/asGate #CH2/CV/none #generator/gate 

https://youtu.be/NdHY-eDipkY

Threshold Logic Neuron is a three-input programmable logic gate.

Controls
* Digital Ins: Logical states of Dendrites 1 and 2
* CV Ins: CV 1 is the logical state of Dendrite 3 (5 volts is high, or True)
* Outputs: A/C and B/D are the output of the Axon. Both outputs are the same so that one may be patched back to an input, if desired.
* Encoder Push: Cycle cursor between Dendrite 1, 2, and 3 weight, and Axon threshold
* Encoder Turn: Set the selected weight or threshold

Threshold Logic Neuron is a three-input/single-output logic gate. Each of three inputs ("Dendrites") is given a weight (in the case of Hemisphere, a weight of between -9 and 9). The output ("Axon") is given a threshold (in Hemisphere, between -27 and 27). When the sum of the weights of high inputs exceeds the threshhold, the output goes high.

The neuron can be used to reproduce common logic gates; for example:

* Dendrite 1: w=3
* Dendrite 2: w=3
* Dendrite 3: w=3
* Axon Output: t=8

This reproduces and AND gate, because all Dendrites need to go high (for a sum of 9) to exceed the threshold of 8.

* Dendrite 1: w=3
* Dendrite 2: w=3
* Dendrite 3: w=3
* Axon Output: t=2

This reproduces an OR gate, because only one Dendrite needs to go high to exceed the threshold of 2.

The values can also be negative. So

* Dendrite 1: w=-3
* Dendrite 2: w=-3
* Axon Output: t=-5

This is a two-input NAND gate, because the output is high (because 0>-5) unless both Dendrite 1 and 2 are high, which brings the sum below the threshold.

But you're not limited to reproducing standard Boolean operations. You can create your own logical operations. For example, you can do this:

* Dendrite 1: w=2
* Dendrite 2: w=2
* Dendrite 3: w=5
* Axon Output: t=3, and mult the output into Dendrite 3

This creates a type of state memory: when Dendrites 1 and 2 go high, the output goes high (2+2>3), and the output is sent back to Dendrite 3, which forces the output to remain high, whatever happens to Dendrites 1 and 2 later.

A variation of that theme is

* Dendrite 1: w=2
* Dendrite 2: w=-2
* Dendrite 3: w=2
* Axon Output: t=1, and mult the output into Dendrite 3

Now, Dendrite 1 fires the axon, which feeds back into itself. Dendrite 1 can go low again and the output stays high. But a high signal at Dendrite 2 will reset the memory unless Dendrite 1 is still on.