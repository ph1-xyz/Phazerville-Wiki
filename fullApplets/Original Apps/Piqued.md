_Piqued_ is a a port of the envelope generator function from the open-source [Mutable Instruments Peaks](http://mutable-instruments.net/modules/peaks) module. _Piqued_ provides four independently-triggerable envelopes on output channels A to D, with independently mappable voltage-control via the CV1 to CV4 inputs over envelope duration parameters for each segment of each envelope. (v1.1 or later: Voltage control over the Euclidean trigger filter parameters and the trigger delay time is also possible - see below.) Triggers for each of the four envelopes can also be mapped from any of the four trigger inputs (TR1 to TR4). Segment shape (curves) can be set for each segment of each of the four envelopes. A variety of envelope types are available, also independently settable for each envelope, including repeating (looping) envelope types. The shape of each envelope can be visualised while setting parameters. There is also a "Euclidean trigger filter" included, which turns the _Piqued_ app into a quad-channel Euclidean polyrhythm generator, that can output envelopes, not just gate/trigger signals. See the [O&C videos page](https://github.com/mxmxmx/O_C/wiki/Ornament-and-Crime-videos-and-tracks) for some demonstrations of _Piqued_.

### Controls

_Piqued_ presents quite a rich UI (user interface), which is harder to describe in words than it is to use. The following explanations should make sense as soon as you see the UI in action. Once experienced, the interface becomes quite intuitive, we think.

|       | Left Encoder                                                                                                                                  | Right Encoder                                                                                                                                                                                                                                                                                                  |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TURN  | In menu settings mode, elect the type of envelope. In envelope visualisation mode, select channel A to D to edit (all channels always active) | Navigation mode: move up and down through the menu items (when in menu setting mode), or move back and forth between envelope segments (envelope visualisation/segment duration setting mode). Edit mode: increase or decrease the value being edited (segment durations when in envelope visualisation mode). |
| PRESS | Toggle between menu settings and envelope visualisation and segment duration settings.                                                        | Toggle between menu navigation (selection)/envelope segment selection mode and value editing mode                                                                                                                                                                                                              |
| LONG  | copy selected scale/mask to _all_ channels/slots                                                                                              | App selection menu                                                                                                                                                                                                                                                                                             |

|            | Up Button                                                                                                                                                      | Down Button                                                                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| PRESS      | Increase duration for currently selected envelope segment for currently displayed envelope generator (A to D) by 32 (when in envelope visualisation mode only) | Decrease duration for currently selected envelope segment for currently displayed envelope generator (A to D) by 32 (when in envelope visualisation mode only) |
| LONG PRESS |                                                                                                                                                                |                                                                                                                                                                |

### Available settings (per-channel)

|Setting | Meaning |
|---|---|
|(envelope type)| the type of envelope (segment nomenclature is standard: A=attack, D=decay, S=sustain (level) and R=release). Available envelope types are described in the table below.|
|`Trigger input`| specifies which trigger/gate input, TR1 to TR4, is used to trigger or gate the envelope on the channel currently displayed. |
|`Tr delay mode`| sets the mode for the trigger delay. If enabled, the trigger delay will postpone the "firing" of the envelope (that is, the commencement of the attack segment of the envelope) for the time set by `Tr delay msecs` and `Tr delay secs` (see below). Available trigger delay modes  are `Off`, `Queue` and `Ring`. `Queue` means that subsequent triggers received while a delay period is active are added to a queue for later action, up to a maximum queue depth set by the `Tr delay count` setting (maximum 32). Further triggers during the delay period are ignored until the number of queued triggers falls below the value set by `Tr delay count`. `Ring` is similar except that triggers received after the queue is full will replace the final trigger in the queue.|
|`Tr delay count`| sets the number of trigger delays that will be stored or buffered for later processing. |
|`Tr delay msecs` | trigger delay in milliseconds (range 0 to 999 milliseconds). If you set a trigger delay of greater than zero, then the envelope for that channel will not "fire" (commence its attack segment) until the specified delay has elapsed. The delay in milliseconds and the delay in seconds are added together, allowing very fine control over the delay. The "countdown" time for the delayed trigger is shown as a fall bar on the righthand side of the trigger indicator for that channel (at the top of the display). |
|`Tr delay secs` | trigger delay in seconds (range 0 to 64 seconds) - see `Tr delay msecs` above`. |
|`Eucl length`| sets the length of the Euclidean pattern (range 2 to 32 in "beats", where each beat is a received trigger/gate pulse) used to filter triggers for that channel. For a detailed explanation of Euclidean patterns and their use in rhythm generation, see [this paper](http://cgm.cs.mcgill.ca/~godfried/publications/banff.pdf) by Godfried Toussaint, or for a brief explanation, see [this presentation}(http://www.maths.usyd.edu.au/u/joachimw/talk2.pdf).  `Eucl length` defaults to `Off`, which means there is no filtering of triggers.| 
|`Eucl fill`| sets the number of beats in the pattern that let triggers through to "fire" the envelope. If the fill number is equal to or greater than the Euclidean pattern length number, then every incoming trigger will pass the Euclidean filter and fire the envelope for that channel. If the fill number is zero, then none shall pass.|
|`Eucl offset`| sets the offset (or more accurately, the rotation) of the Euclidean pattern. The combination of pattern length (`Eucl length`) and number of active beats (`Eucl fill`) within that pattern length uniquely determines the Euclidean pattern, using the Bjorklund algorithm. For example, if `Eucl length` is set to 8 and `Eucl fill` is set to 5, and `Eucla offset` is set to the default of 0, then the pattern will be 10110110, where 1 is an active beat (triggers are allowed to pass) and 0 is inactive (triggers are blocked). By setting `Eucl offset` to 1, the pattern becomes 01101101, if set to 2 the pattern becomes 11011010 and so on.| 
|`CV1 ->` | sets the mapping from the CV1 input. The value on CV1 can be ignored (`None`) or sent to control the duration of one of: Att(ack), Dec(ay), Sus(tain) (level, not duration) and Rel(ease), or (in v1.1 or later) it can be set to control the Euclidean trigger filter parameters: `Eleng` (Euclidean pattern length), `Efill` (Euclidean pattern fill, `Eoffs` (Euclidean pattern offset/rotation), or the trigger delay time (`Delay`). Note that when set to `Eleng` or `Efill`, negative voltages can be used to block all triggers. The input CV values are added to whatever is set for the duration/level or Euclidean parameters or trigger delay time via the menu settings. |
|`CV2 ->` | same as `CV1 ->`, but for the CV2 input |
|`CV3 ->` | same as `CV1 ->`, but for the CV3 input |
|`CV4 ->` | same as `CV1 ->`, but for the CV4 input |
|`Hard reset`| If set to on, the envelope will instantly restart at zero on the next received trigger/gate, rather than starting from the amplitude that it is at at the time that the trigger/gate signal is received. |
| `Gate high` | when set to `Yes`, forces the trigger/gate to high. This is useful when using the looping envelope types, which then just loop continuously, regardless of what is happen on their trigger/gate input, and thus they act as LFOs. |  
|`Attack shape`| sets the shape of the attack segment for the currently displayed envelope. Available shapes are listed in the table below.|
|`Decay shape`|sets the shape of the decay segment for the currently displayed envelope. Available shapes are listed in the table below. |
| `Release shape` |sets the shape of the release segment for the currently displayed envelope. Available shapes are listed in the table below. |


|Envelope type | Description |
|--------------|-------------|
| `AD`         | Attack-Decay: the attack segment commences on receipt of a trigger or on the rising edge of a gate signal, and the decay segment follows immediately after the attack segment has reached its peak, regardless of whether the gate or trigger signal is still high. |
| `ADSR`       |Attack-Decay-Sustain-Release: just like every other ADSR envelope |
| `ADR` | Attack-Decay-Release: the attack segment commences on receipt of a trigger or on the rising edge of a gate signal, and the decay segment follows immediately after the attack segment has reached its peak. The sustain level is an inflection point for the decay - when the decay reaches the sustain level, the release segment immediately commences, regardless of whether the gate or trigger signal is still high. See the _Tips_ section below on how to use the ADR mode as an AHR/AHD (attack-hold-release or attack-hold-decay) envelope generator with trigger signals.|
| `ASR` | Attack-Sustain-Release: the attack segment commences on receipt of a trigger or on the rising edge of a gate signal, and the envelope stays at maximum level for as long as the gate input for it remains high (sustain), and then commences the release segment as soon as the gate signal goes low. |
| `ADSAR` | is like an ADSR envelope, except that the attack segment re-triggers as soon as the sustain segment is finished, before proceeding to the release segment. |
| `ADAR` | is like the ADR envelope, except that the attack segment re-triggers as soon as the decay segment has finished, before going into the release segment.|
| `AD loop` | is like the AD envelope, except that it automatically re-triggers for as long as the trigger/gate input for it is high (see also the `Gate high` setting) |
| `ADR loop` |  is like the ADR envelope, except that it automatically re-triggers for as long as the trigger/gate input for it is high (see also the `Gate high` setting) |
| `ADAR loop` |  is like the ADAR envelope, except that it automatically re-triggers for as long as the trigger/gate input for it is high (see also the `Gate high` setting) |

| Segment shape  | Description |
|----------------|-------------|
| `Lin`          | Linear (a straight line, equation _x_ = _t_ where _t_ is time) |
| `Exp` | Exponential (equation _x_ = 1 - _e_<sup>-4_t_</sup>) |
| `Quart` | Quartic (equation _x_ = _t_<sup>3.32</sup>) |
| `Sine` | half a sine wave (equation _x_ = sin(8 * pi * _t_) )|
| `Ledge` | almost a square wave, but with rounded corners, when used for attack, gives an immediate (punchy) rise, then a plateau. When used for decay or release, it has a plateau before falling. |
| `Cliff` | similar to `Ledge`, but when used for attack, has a delay before rising, when used for decay or release, it falls immediately.|
| `Gate` (v1.1) | is used when gate outputs are desired. The value rises immediately to maximum in the attack segment, and the value falls immediately to minimum in the decay and release segments. In other words, a pulse is output.|
| `BgDip` | Big dipper - has one large bump on the way up or down. |
| `MeDip` | Medium dipper - has a medium sized dip on the way up or down. |
| `LtDip` | Little dipper - has a little dip (more a ledge) on the way up or down. |
| `Wiggl` | Wiggles - lots of wiggles on the way up or down. |

### Inputs and outputs

Trigger input and CV1 to CV4 are mappable per-channel via the menu, as described above. Outputs for envelopes A to D appear on outputs A to D respectively.

### Screensaver display

The screen is divided into quadrants, each showing a rolling display of the output values on each of channels A to D. Superimposed on this rolling value line is a representation of the envelope for that channel, as it progresses through its segments.

### Tips and tricks
 - the ADR mode can also be used as an AHR (attack-hold-release, sometimes also called AHD (attack-hold-decay)) envelope generator. AHR envelope are useful when you want to generate an envelope with a flat sustain period, which usually requires a gate input with some duration. If you only have trigger signals, that is, short pulses, then you can create an AHR envelope by choosing ADR mode, and setting the sustain inflection point to 255 (maximum). By doing that, the decay segment falls from maximum value to... maximum value - in other words, it's flat! The decay segment time/duration then sets the hold duration after a trigger is received. Also try setting the sustain level in ADR mode to something a little bit less than 255 (say 230), and set the decay shape to Wiggle. Now you have an AHR envelope with a wiggly and slightly downsloping plateau segment. Several variations on this theme are possible.
