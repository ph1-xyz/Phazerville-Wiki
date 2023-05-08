Synchronization is one of the biggest challenges in the hardware world, which is why the internal clock functionality of the Hemisphere Suite has been a point of focus for me. The **Clock Setup** screen - accessed by dual-pressing both _UP+DOWN_ buttons - provides several controls for making the o_C run standalone, and sync to pulses on TR1 while it's running.

### Parameters
* **Play/Stop/Pause** (toggle) - indicated by a Clock icon followed by a Pause, Play or Stop icon
  - Can also be toggled with _Left Encoder Long-Press_
  - When Paused, a single pulse on TR1 will immediately start the clock
* **Fwd** - physical Clock Forwarding legacy option
  - Duplicates physical TR1 to TR3 (when clock is not running on TR3)
* **PPQN** - expected resolution of external clock pulses on TR1
  - set to 0 to ignore incoming pulses
* **Tempo** - pretty self-explanatory :P
  - Manual Tap-Tempo - press the encoder button 4 times on this parameter to detect and set the BPM accordingly
* **Multipliers/Dividers** - virtual triggers generated for each channel in relation to Tempo
  - set to 0 to disable internal clock on that channel; physical triggers will pass thru instead
* **Manual Triggers** - The four Button icons at the bottom enable you to manually fire each trigger
  - handy for advancing or resetting sequencers, etc.

### Notes
Realtime MIDI messages for Start, Stop, & Clock (at 24ppqn) are sent via USB automatically. An option to disable this is planned.

Clock Setup is available in Hemispheres as well as the [Calibr8or](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Calibr8or) app. However, the Clock settings are only stored in the active Preset in Hemisphere.
There is currently experimental support for incoming MIDI Start/Stop/Clock sync in Calibr8or; the same feature is planned for Hemispheres, but will require an overhaul of MIDI message handling.