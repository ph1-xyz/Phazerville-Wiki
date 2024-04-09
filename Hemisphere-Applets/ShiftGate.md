#sequencer #masterClockOnCH1 #gateOnCH2 #triggerGenerator

ShiftGate is a dual shift register-based gate/trigger sequencer for creating aleatoric rhythm patterns.

Controls
* Digital Inputs: Digital 1 clocks the sequencer by shifting both registers to the left, and Digital 2 freezes the sequencer and locks out changes.
* CV Inputs: Flip input for each channel. When CV is high, the bit rotating off the left side of the corresponding channel's register will be replaced at bit 0 with the opposite value.
* Outputs: Trigger or gate output for each channel
* Encoders: Change the length and output type for each channel

ShiftGate has two channels controlled by a single clock input. Each channel starts with a random 16-bit register*. When a clock is received at Digital 1, the following things happen:

1. The register is shifted to the left. 
1. If Digital 2 is high, the register is frozen; the high bit (based on length) of the previous value is moved back to the beginning (bit 0), and skip to 4.
1. If the CV input for the corresponding channel is low, the high bit (based on length) of the previous value is moved back to the beginning (bit 0). If the CV input is high, the high bit is flipped, and that value is put at the beginning. This is known as an XOR operation.
1. The value of bit 0 is examined. If the channel's Type is set to "Trig," then a trigger will be sent from the channel's output if the value is 1. If the channel's type is set to "Gate," the gate state is high if the value is 1. The gate will then _remain_ high until the next time the register's bit 0 is 0.

ShiftGate is in Hemisphere Suite from v1.5.

_* When ShiftGate's state is saved via SysEx or system save, Output A's register is saved, and Output B's register is randomized._