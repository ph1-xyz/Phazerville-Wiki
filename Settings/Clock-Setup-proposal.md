![PXL_20231228_051510847~2.jpg](https://github.com/djphazer/O_C-Phazerville/assets/109086194/16bb6eda-0d75-4ca0-9379-093eb5bf3ab8)

##### Externally Clocked
Externally Clocked Icon to be used instead of Clock
<!-- // { 0x02, 0x5e, 0x02, 0x5e, 0x02, 0x5e, 0x02, 0x5e }-->
![[internallyClockedIconProposal.png]]

TR1/3 ins trigger or advance the app

// If trigger mult/divs are not working in this mode, hide them
// Are outgoing MIDI messages for Start, Stop, & Clock (at 24ppqn) sent via USB automatically also while in Externally Clocked mode? Can this be disabled or modified (PPQN parameter values "quantization" like in Mutable Instruments Grids?)
// Should user be allowed to set PPQN to 0 to stop acceptation? If yes, how to make clear to the user that effect? Maybe this Stop-feature could directly be put [somewhere](Settings/Clock-Setup-proposal#User-Interaction) more intuitive and direct.  
###### User-Interaction
Pressing a button or an icon could temporarily- or latch-stop TR acceptation.
###### External Interaction through Inputs
MIDI CC Message or repurposed TR2/4 IN could work as
- GATE for external triggers on TR1/3 to be accepted or ignored
- TRIG to latch trigger-acceptation on TR1/3
##### Routed Interactions
???

##### Internally Clocked
Internally Clocked Icon to be used instead of Clock
<!-- { 0xbe, 0x02, 0xb8, 0x03, 0x03, 0xb8, 0x02, 0xbe }-->
![[externallyClockedIconProposal 1.png]]

App are triggered from Internal clock.
- **Mult/div** of this clock are *shown*
- **Trigger Input Remapping** is *hidden* unless channel multiplier is set to x0

Incoming MIDI Start/Stop/Clock messages intuitively start the internal clock and feed it sync pulses at 2ppqn. The clock speed can then be reinterpreted differently with the `Sync=` parameter.

// (Does this work both from External and Internal Clock?) Outgoing MIDI messages for Start, Stop, & Clock (at 24ppqn) are sent via USB automatically. An option to disable this is planned.

// Could Remapping be assigned to use with gates?
###### User Interaction
Pressing a button could work as latch-stop (pressing again resumes) of clocks or as a gated-stop (releasing the button resumes the clock)

###### Tap Tempo
press the encoder button 4 times on this parameter to detect and set the BPM accordingly
###### External Interaction through Inputs
MIDI CC Message or repurposed TR2/4 IN could work as
- GATE for clock(s) to run
- TRIG to latch clock(s) to run

// Could Clock resolution (PPQN) effect the MIDI OUT of this?
// Allow modal navigation of Clock Menu = rotating the encoder cycles through sections, clicking enters them; problem of how to exit this without going back to current applet or main menu or screensaver? A section made like this could be transported out of the Clock setup and be actioned during applets running?


(Updated for v1.6.999+)
The **Clocks/Triggers** screen, fka Clock Setup, is accessed by dual-pressing both _UP+DOWN_ buttons. The top half of the screen provides internal clock controls for standalone operation. The multipliers determine how internally generated clock triggers are fed to the applets. The clock will sync to external pulses on TR1 while it's running. The bottom half of the screen has settings for remapping the physical trigger inputs (to avoid the need for mults) as well as manual triggers for convenience.

##### SYNC
Could this function be renamed to PPQN as in Mutable Instruments Grids?

Icon for SYNC?
<!--  { 0x0f, 0x05, 0x77, 0x40, 0xef, 0x05, 0xc7, 0xf0 }-->
![[ppqnProposal4.png]]

##### SWING
Is this applied both in Externally- and Internally-clocked mode?

Icon for SWING instead of Metronome
<!--  { 0xc0, 0x08, 0x00, 0xc0, 0x08, 0x00, 0xc0, 0x08 }-->
![[swingProposal3.png]]


* **Play/Stop/Pause** (toggle) - indicated by a Clock icon followed by a Pause, Play or Stop icon
