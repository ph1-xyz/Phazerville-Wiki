## Videos
- [Performance Controller Demo on OCP X](https://www.youtube.com/watch?v=N-0qtiLb8bg)
- [Smooth Crossfade Demo](http://www.youtube.com/watch?v=6YzXK8O0tT4 "O_C Scenes App Demo")
- [Trigger Demo](https://www.instagram.com/p/CxaiU_rr6ue/)
- [Random Sequence Demo](https://www.instagram.com/p/Cxmyv6euch0/)

## Macro CV Switcher/Crossfader

Inspired by the hype of [**Traffic**](https://www.youtube.com/watch?v=SR0HXqEbuaY) by Jasmine & Olive Trees, this app offers 4 "scenes" with 4 CV output values each. There are also 4 preset banks, using the same mechanism as Calibr8or and Hemisphere (long-press DOWN button to access).

You must store your settings to a Preset _before_ doing an **[EEPROM Save](https://github.com/djphazer/O_C-BenisphereSuite/wiki/EEPROM-Save)**!

### Inputs

- TR1-TR4 - Jumps to corresponding Scene.
  - Similar to Traffic, these are prioritized so TR1/Scene1 will take precedence if multiple inputs are gated simultaneously.
- CV1 - bipolar smooth crossfade between scenes, centered on the last triggered scene.
  - 1 Volt == 1 Scene. 4 Volts loops back around.
- CV2 - (v1.6.5) bias offset for all values
- CV3 - (v1.6.6) modulates slew/smoothing factor for all outputs
- CV4 - when gated (>2V), enables a random 16-step sequence on Scene 4 using a shuffled combination of all 16 CV values.
  - TR4 will advance the sequence.
  - A new sequence is generated every time the gate goes high

### Controls

- UP/DOWN buttons move edit cursor between the 4 scenes.
- Left Encoder - press to toggle between editing A or B output for selected scene
- Right Encoder - press to toggle between editing C or D output for selected scene
- Long-press Left Encoder - toggle Trig Sum mode on output D
- Long-press DOWN button for Preset Menu
- [global] Long-press UP button to invoke screensaver view