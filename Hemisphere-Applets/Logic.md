#logic #gateGenerator 
https://youtu.be/mHZCaMH_Dgk

Logic is a two-input logic module that performs two logical operations at once.

Controls
* Digital Ins: Two logical operands, in the form of gate signals with high being True and low being False
* CV Ins: Inputs 1 and 2 set the logical gate when the gate selected for the corresponding channel is "CV"
* Outputs: Results of the logical operations as a high (5 volt, when True) or low (0 volt, when False) signal
* Encoder Push: Alternates the cursor between the two channels
* Encoder Turn: Selects the logical gate or "CV" for each channel

Available gate types are
* **AND**: True when both inputs are True
* **OR**: True when either or both inputs are True
* **XOR**: True when both inputs are different than the other input
* **NAND**: True when either input is False
* **NOR**: True when both inputs are False
* **XNOR**: True when both inputs are the same

Another option, "CV," is available. When set to "CV," the logical gate type will be set via CV using the corresponding CV input.