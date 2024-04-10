#controller #dualInput #dualOutput #independentChannels 

Ever just need a button, to trigger something or toggle something? Me too! Button functions as a dual trigger and/or latching toggle (both 5V when high).

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Press button 1   | Press button 2 |
| CV In          | No effect |     No effect       |
| Output         |          Trigger/Gate 1           |         Trigger/Gate 2          |

### UI Parameters
* Channel selection (scroll clockwise)
* Button mode: trigger, latch (scroll counterclockwise)
* Press selected button (push encoder)

_Note: Button2 overrides your Hemisphere cursor mode. In this applet, scrolling clockwise switches between selecting button channels, scrolling counterclockwise switches the selected channel between a trigger mode (clock icon) and a latching toggle mode (switch icon)_


Adapted from [Button](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Button) © 2018-2022, Jason Justian and Beige Maze Laboratories. 