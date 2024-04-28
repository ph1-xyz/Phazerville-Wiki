
Scenes is a macro CV Switcher/Crossfader inspired by  [**Traffic**](https://www.youtube.com/watch?v=SR0HXqEbuaY) by Jasmine & Olive Trees. This app offers 4 "scenes" with 4 CV output values each; there are also 4 preset banks, using the same mechanism as [[Calibr8or]] and [[Hemisphere]] (long-press DOWN button to access).

You must store your settings to a Preset _before_ doing an **[EEPROM Save](https://github.com/djphazer/O_C-Phazerville/wiki/EEPROM-Save)**!

### Controls

|       | Left Encoder                                            | Right Encoder                                           |
| ----- | ------------------------------------------------------- | ------------------------------------------------------- |
| TURN  |                                                         |                                                         |
| PRESS | Toggle between editing A or B output for selected scene | Toggle between editing C or D output for selected scene |
| LONG  | Toggle Trig Sum mode on output D                        |                                                         |

|            | Up Button                              | Down Button                            |
| ---------- | -------------------------------------- | -------------------------------------- |
| PRESS      | Move edit cursor between the 4 scenes. | Move edit cursor between the 4 scenes. |
| LONG PRESS | Invoke screensaver view                | Go to Preset Menu                      |

### Inputs

|     | 1                                                                                                                                | 2                                             | 3                                               | 4                                                                                                                                                                                                                       |
| --- | -------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TR  | Jumps to corresponding Scene.<br><br>Prioritized so TR1/Scene1 will take precedence if multiple inputs are gated simultaneously. | Jumps to corresponding Scene.<br><br>(v1.6.5) | Jumps to corresponding Scene.<br><br> (v1.6.6)  | Jumps to corresponding Scene.                                                                                                                                                                                           |
| CV  | bipolar smooth crossfade between scenes, centered on the last triggered scene. 1 Volt == 1 Scene. 4 Volts loops back around.     | bias offset for all values                    | modulates slew/smoothing factor for all outputs | when gated (>2V), enables a random 16-step sequence on Scene 4 using a shuffled combination of all 16 CV values.<br><br>TR4 will advance the sequence.<br><br>A new sequence is generated every time the gate goes high |
| OUT |                                                                                                                                  |                                               |                                                 |                                                                                                                                                                                                                         |



## Videos
- [Performance Controller Demo on OCP X](https://www.youtube.com/watch?v=N-0qtiLb8bg)
- [Smooth Crossfade Demo](http://www.youtube.com/watch?v=6YzXK8O0tT4 "O_C Scenes App Demo")
- [Trigger Demo](https://www.instagram.com/p/CxaiU_rr6ue/)
- [Random Sequence Demo](https://www.instagram.com/p/Cxmyv6euch0/)
