![PXL_20231228_051510847~2.jpg](https://github.com/djphazer/O_C-BenisphereSuite/assets/109086194/16bb6eda-0d75-4ca0-9379-093eb5bf3ab8)

(Updated for v1.6.999+)
The **Clocks/Triggers** screen, fka Clock Setup, is accessed by dual-pressing both _UP+DOWN_ buttons. The top half of the screen provides internal clock controls for standalone operation. The multipliers determine how internally generated clock triggers are fed to the applets. The clock will sync to external pulses on TR1 while it's running. The bottom half of the screen has settings for remapping the physical trigger inputs (to avoid the need for mults) as well as manual triggers for convenience.

### Parameters
* **Play/Stop/Pause** (toggle) - indicated by a Clock icon followed by a Pause, Play or Stop icon
  - Can also be cycled with _Left Encoder Long-Press_ on any screen within Hemisphere
  - When Paused, the clock is armed - a single pulse on TR1 will immediately start the clock
* **Tempo** - pretty self-explanatory :P
  - Manual Tap-Tempo - press the encoder button 4 times on this parameter to detect and set the BPM accordingly
* **Swing/Shuffle** (new in v1.6.999) - delays every other clock pulse within a beat
  - (this setting is not currently saved)
* **Sync** - aka PPQN; expected resolution of external clock pulses on TR1
  - set to 0 to ignore incoming pulses
* **Multipliers/Dividers** - virtual triggers generated for each channel in relation to Tempo
  - set to 0 to disable internal clock on that channel; physical triggers will pass thru instead
* **Trigger Input Remapping** (new in v1.6.999) - reroute physical trigger inputs to the applets
  - only applies when the internal clock is not running, or if multiplier is set to "x0" for that channel
  - to mimic legacy "Clock Forwarding" function, simply set channel 3 to "TR1" instead of "TR3" (saved settings will automatically load like this)
* **Manual Triggers** - The four Button icons at the bottom enable you to manually fire each trigger
  - handy for advancing or resetting sequencers, etc.

### Notes
* Outgoing MIDI messages for Start, Stop, & Clock (at 24ppqn) are sent via USB automatically. An option to disable this is planned.
* Incoming MIDI Start/Stop/Clock messages intuitively start the internal clock and feed it sync pulses at 2ppqn. The clock speed can then be reinterpreted differently with the `Sync=` parameter.
* The internal Clock is available in Hemispheres as well as the [Calibr8or](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Calibr8or) app. However, Clock settings are only stored in the active Preset in Hemisphere.