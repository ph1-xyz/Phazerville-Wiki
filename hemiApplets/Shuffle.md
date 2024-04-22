#masterClockOnCH1 #gateOnCH2 #resetOnCH2 #triggerGenerator 

Shuffle is a two-step clock offset. Each step can be delayed by between 0% and 99% of the incoming clock tempo.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls:
* Digital Ins: Digital 1 is the clock, and a trigger to Digital 2 resets to the first-numbered step
* CV Ins: Bi-polar modulation of the percentage delay for each step
* Outputs: Output 1 is the outgoing, potentially-delayed, clock
* Encoder: Set the percentage delay of each step

Note that reset does not, itself, trigger a clock. It just brings the step back to the beginning so that another clock can trigger the first step.