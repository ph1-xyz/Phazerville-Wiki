## Macro CV Switcher/Crossfader

Inspired by the hype of [**Traffic**](https://www.youtube.com/watch?v=SR0HXqEbuaY) by Jasmine & Olive Trees, this app offers 4 "scenes" with 4 CV output values each. There are also 4 preset banks, using the same mechanism as Calibr8or and Hemisphere (long-press DOWN button to access).

As with Calibr8or, you must store your settings to a Preset _before_ doing an **[EEPROM Save](https://github.com/djphazer/O_C-BenisphereSuite/wiki/EEPROM-Save)**!

### Inputs

- TR1-TR4 - Jumps to corresponding Scene.
  - Similar to Traffic, these are prioritized so TR1/Scene1 will take precedence if multiple inputs are gated simultaneously.
- CV1 - smooth crossfading offset, starting at the last triggered Scene. 1V/Scene.
- CV2, CV3 - _not implemented_
- CV4 - when gated (>2V), enables a random 16-step sequence on Scene 4 using a shuffled combination of all 16 CV values.
  - TR4 will advance the sequence.
  - A new sequence is generated every time the gate goes high

### Controls

- UP/DOWN buttons move edit cursor between the 4 scenes.
- Left encoder press toggles between editing A or B output for selected scene
- Right encoder press toggles between editing C or D output for selected scene
- Long-press DOWN button for Preset Menu
- [global] Long-press UP button to invoke screensaver view
