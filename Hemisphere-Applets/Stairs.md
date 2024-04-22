#masterClockOnCH1 #resetOnCH2 #gateOnCH2 #CVgenerator #BoC-EoC 

Stairs is a stepped, clocked voltage generator based on the Noise Engineering Clep Diaz's 'step' and 'rand' modes. On each input clock pulse, the output voltage advances to the next 'step,' where the first step is always 0v and the last always 5v, with even voltage divisions on the intermediate steps.

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Controls

- Digital Ins: 1:Clock,  2:Reset(can be held)
- CV Ins:   1:Number of Steps,  2:Current Step (Disables clock if > 0v)
- CV Outs:  A:Stepped CV output 0-5v, B:Beginning-of-Cycle pulse 
- Encoder: Sets number of steps, step direction, and toggles random on/off

## Steps
Controls the total number of steps taken from 0 to 5v or 5v to 0 volts.

## Direction
Sets the direction the voltage changes in on each step: up, up+down, or down. This effectively gives up ramp, triangle, and down ramp shapes. The step count is effectively doubled in up+down mode, except that the bottom and top steps are not repeated when changing directions.

## Random
Turning random ON makes each step's voltage deviate a little bit from where it would be, but the overall direction of movement is preserved.

