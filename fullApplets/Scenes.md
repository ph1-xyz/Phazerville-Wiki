*Scenes* is a macro CV-switcher/crossfader inspired by the hype of [**Traffic**](https://www.youtube.com/watch?v=SR0HXqEbuaY) by Jasmine & Olive Trees.

The app offers 4 "scenes" with 4 CV output values each. There are also 4 preset banks, using the same mechanism as [[Calibr8or]] and Hemisphere (long-press DOWN button to access).

You must store your settings to a Preset _before_ doing an **[EEPROM Save](https://github.com/djphazer/O_C-Phazerville/wiki/EEPROM-Save)**!

### I/O

|        |                                                                       1                                                                       |                       2                       | 3                                                             | 4                                                                                                                                                                            |
| ------ | :-------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------: | ------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TR     | Gate IN allows jumping to corresponding Scene; similarly to Traffic, this IN will have precedence if multiple inputs are gated simultaneously | Gate IN allows jumping to corresponding Scene | Gate IN allows jumping to corresponding Scene                 | Gate IN allows jumping to corresponding Scene; when *random step sequencer* is enabled through gated-CV4, a trigger here will advance it                                     |
| CV INs |         bipolar smooth crossfade between scenes, centered on the last triggered scene; 1 Volt == 1 Scene. 4 Volts loops back around.          |   (from v1.6.5) bias offset for all values    | (from v1.6.6) modulates slew/smoothing factor for all outputs | when gated (>2V), enables a *random 16-step sequence* on Scene 4 using a shuffled combination of all 16 CV values; a new sequence is generated every time the gate goes high |
| OUTs   |                                                                   CV output                                                                   |                   CV output                   | CV output                                                     | CV output                                                                                                                                                                    |
### Controls

|       | Left Encoder                                            | Right Encoder                                           |
| ----- | ------------------------------------------------------- | ------------------------------------------------------- |
| TURN  |                                                         |                                                         |
| PRESS | toggle between editing A or B output for selected scene | toggle between editing C or D output for selected scene |
| LONG  | toggle Trig Sum mode on output D                        |                                                         |

|            | Up Button                                           | Down Button                           |
| ---------- | --------------------------------------------------- | ------------------------------------- |
| PRESS      | move edit cursor between the 4 scenes               | move edit cursor between the 4 scenes |
| LONG PRESS | invoke screensaver view               | Access Preset Banks                   | Preset Menu                           |

## Videos
- [Performance Controller Demo on OCP X](https://www.youtube.com/watch?v=N-0qtiLb8bg)
- [Smooth Crossfade Demo](http://www.youtube.com/watch?v=6YzXK8O0tT4 "O_C Scenes App Demo")
- [Trigger Demo](https://www.instagram.com/p/CxaiU_rr6ue/)
- [Random Sequence Demo](https://www.instagram.com/p/Cxmyv6euch0/)

