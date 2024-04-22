#triggerGenerator #dualOutput 

A deluxe Euclidean pattern generator, two channels, up to 32 steps each. Using UI code from qiemem; named after adegani's version of the applet with the flexible CV Input routing. The extra zero-padding parameter makes it worthy of the *X* ;-)

### I/O

|        | 1/3 | 2/4 |
| ------ | :-: | :-: |
| TRIG   |     |     |
| CV INs |     |     |
| OUTs   |     |     |


Each channel has four parameters:
* Length
* Hits
* Offset (right-shift)
* Padding (0's added to the end before Offset)

There are two additional parameters for CV Input Modulation Targets. Bipolar voltages on each CV Input will modulate a single parameter on either channel.

### Digital Inputs
* 1: Clock
* 2: Reset

### CV Inputs
The CV inputs will modulate whatever parameter the tiny _1_ or _2_ is sitting next to.

### Outputs
Each channel outputs a standard trigger pulse when clocked. Global Pulse Length can be adjusted in Hemisphere Config.

## Future
* Expand the pattern generator to 64 bits...
* Some kind of UI tweaks to better visualize patterns longer than 16.