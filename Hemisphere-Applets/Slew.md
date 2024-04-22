#dualCVInput #dualOutput #CVgenerator 

Slew is a simple slew (or lag) processor. Two independent channels share the same settings. Channel 1's output is linear, and Channel 2's output is exponential.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls
* Digital Ins: Slew defeat for Channels 1 and 2
* CV Ins: Input signals for Channels 1 and 2
* Outputs: A/C is the linear Channel 1 output, and B/D is the exponential Channel 2 output
* Encoder Push: Select between Rise and Fall
* Encoder Turn: Increase and decrease Rise or Fall time

When Rise or Fall values are changed, a time (in ms) will briefly appear on the display. This indicates the approximate time that it would take for the linear signal to rise or fall 5 volts. The time between actual voltages will be proportionate to this time, and the exponential signal will take less time.

When a high gate is present at either digital input, the corresponding channel's slew will be defeated. That is, the input will pass through to the output.