#generator/trigger #CH1/trig/mainClock #CH2/trig/none #CH2/CV/none #aleatoric #dualOutput/triggers #CH1/trig/mainClock 

*Brancher* is a Bernoulli Gate, inspired by Mutable Instruments Branches. It sends incoming gate or clock to one of two outputs, based on a selected probability.

### I/O

|        |                1/3                 |    2/4     |
| ------ | :--------------------------------: | :--------: |
| TRIG   | Signal (clock or gate) for routing | No effect  |
| CV INs |  Probability modulation (bipolar)  | No effect  |
| OUTs   |             Output A/C             | Output B/D |

### UI Parameters
* Probability
* Press encoder to override probability-selected output and switch to the other one


Adapted from [Brancher](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Brancher) © 2018-2022, Jason Justian and Beige Maze Laboratories. 
