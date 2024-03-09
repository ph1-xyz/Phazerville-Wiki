You can find links to documentation for (almost) every single O_C function on this page.

[Download a **Release**](https://github.com/djphazer/O_C-BenisphereSuite/releases) or [Request a **Custom Build**](https://github.com/djphazer/O_C-Phazerville/discussions/38).

# Phazerville Suite
Thanks for checking out my firmware. I've basically tried to hoard all the notable Apps and Applets in one repo! All the full-screen apps from [Hemisphere](https://github.com/Chysn/O_C-HemisphereSuite/wiki) are here, plus all of the [stock O&C firmware](https://ornament-and-cri.me/user-manual-v1_3/) apps and a few new ones, albeit in limited combinations depending on which .hex file you grabbed from the [Release page](https://github.com/djphazer/O_C-BenisphereSuite/releases).

As of v1.6.999, you can request a **Custom Build** with a simple bot command on [this discussion post](https://github.com/djphazer/O_C-BenisphereSuite/discussions/38).

Read a bit about my [Development Philosophy](https://github.com/djphazer/O_C-Phazerville/wiki/_Philosophy) to understand my motives behind this project.

## Build Choices

In previous versions of v1.6.x, all builds included **Hemisphere**, **Pong**, and the **Scale** & **Waveform Editor**s, plus a selection of different Apps mentioned in the notes.

Files with "**+VOR**" are only for **Plum Audio / 4ROBOTS** hardware variants equipped with a _Variable Output Range_ circuit - O&C Plus, 1uO_c, & OCP X.

Standard 8HP uO_C, After Later uO_C 1U, or full-size 14HP O_C modules should be installed _without_ VOR - your outputs will behave strangely if you do!

_sideNOTE:_ If applets like Stairs, Carpeggio or Shredder appear unresponsive, you might need to [calibrate your ADC](https://www.youtube.com/shorts/AIadpDclP7M) to eliminate an offset on the inputs. This can be done without a fancy multimeter - go to the **Setup / About** app and just skip all the other Calibration steps.

You can reverse the scrolling direction of either/both of your encoders via the **Setup / About** app at the end of the Calibration process.

## Presets for Hemisphere
Applet settings are not remembered unless you store to a Preset, or turn on Auto Save - both are inside [**Hemisphere Config**](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Hemisphere-Config). When storing a Preset, it immediately triggers an EEPROM Save (with a potential 2ms interruption, fyi) so there is no need to also long-press-save on the main menu.

## Hemisphere Gestures
* [**Clock / Trigger Setup**](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Clock-Setup) — Dual-press both UP + DOWN buttons
  - Adjust BPM, external sync, and per-trigger clock mult/div; remap trigger inputs; and manually perform triggers.
* **Cycle Clock state** [Stop]->[Armed]->[Start] — Long-press Left Encoder
  - Extra VOR button on units that have it also Starts/Stops the Clock (v1.6.999)
* **Cycle VBias offset** -5V, -3V, 0V — Dual-press both Encoders [VOR-only]
* [**Hemisphere Config**](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Hemisphere-Config) — Long-press DOWN button
  - Load/save presets, adjust trigger length, screensaver, and cursor mode.
* **Invoke screensaver/blank screen** — Long-press UP button [global] 
* **Return to main menu** — Long-press Right Encoder [global]
  - Execution continues in the background
  - Long-press Right Encoder again on main menu to manually [Save Settings to EEPROM](https://github.com/djphazer/O_C-BenisphereSuite/wiki/EEPROM-Save) (unnecessary in v1.6.999 for Hemisphere; use [Presets](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Hemisphere-Config) instead)
* _Easter Egg_ — On the main menu, press the Left Encoder to find the secret Debug Screen!

# Documentation
## Apps
* Hemisphere (obviously, lol)
* [Calibr8or](https://github.com/djphazer/O_C-Phazerville/wiki/Calibr8or)
* [Scenes](https://github.com/djphazer/O_C-Phazerville/wiki/Scenes)
* [Captain MIDI](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Captain-MIDI)
* [Pong](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Pong)
* [Enigma](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Enigma)
* [The Darkest Timeline](https://github.com/Chysn/O_C-HemisphereSuite/wiki/The-Darkest-Timeline-2.0)
* [Neural Net](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Neural-Net)
* [Scale Editor](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Scale-Editor)
* [Waveform Editor](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Waveform-Editor)
* [CopierMaschine](https://ornament-and-cri.me/user-manual-v1_3/#anchor-copiermaschine)
* [Harrington 1200](https://ornament-and-cri.me/user-manual-v1_3/#anchor-harrington-1200)
* [Automatonnetz](https://ornament-and-cri.me/user-manual-v1_3/#anchor-automatonnetz)
* [Quantermain](https://ornament-and-cri.me/user-manual-v1_3/#anchor-quantermain)
* [Meta-Q](https://ornament-and-cri.me/user-manual-v1_3/#anchor-meta-q)
* [Quadraturia](https://ornament-and-cri.me/user-manual-v1_3/#anchor-quadraturia)
* [Low-rents](https://ornament-and-cri.me/user-manual-v1_3/#anchor-low-rents)
* [Piqued](https://ornament-and-cri.me/user-manual-v1_3/#anchor-piqued)
* [Sequins](https://ornament-and-cri.me/user-manual-v1_3/#anchor-sequins)
* [Dialectic Ping Pong](https://ornament-and-cri.me/user-manual-v1_3/#anchor-dialectic-ping-pong)
* [Viznutcracker, sweet!](https://ornament-and-cri.me/user-manual-v1_3/#anchor-viznutcracker-sweet)
* [Acid Curds](https://ornament-and-cri.me/user-manual-v1_3/#anchor-acid-curds)
* [References](https://ornament-and-cri.me/user-manual-v1_3/#anchor-references)
* [Passencore](https://llllllll.co/t/passencore-chord-ornament-music-theory-crime/45925)

## Applets

* **[ADSR](https://github.com/djphazer/O_C-Phazerville/wiki/ADSR-EG)** - Dual attack / decay / sustain / release envelope
* **[AD EG](https://github.com/djphazer/O_C-Phazerville/wiki/AD-EG)** - Attack / decay envelope
* **[ASR](https://github.com/djphazer/O_C-Phazerville/wiki/%22A%22SR)** - Analog Shift Register
* **[AttenOff](https://github.com/djphazer/O_C-Phazerville/wiki/AttenOff)** - Attenu-vert, Offset, and Mix inputs (now with +/-200% range, mix control)
* **[Binary Counter](https://github.com/djphazer/O_C-Phazerville/wiki/Binary-Counter)** - 1 bit per input, output as voltage
* **[BootsNCat](https://github.com/djphazer/O_C-Phazerville/wiki/BootsNCat)** - Noisy percussion
* **[Brancher](https://github.com/djphazer/O_C-Phazerville/wiki/Brancher)** - Bernoulli gate
* **[BugCrack](https://github.com/djphazer/O_C-Phazerville/wiki/BugCrack)** - Sick drums, don't bug out
* **[Burst](https://github.com/djphazer/O_C-Phazerville/wiki/Burst)** - Rapid trigger / ratchet generator
* **[Button2](https://github.com/djphazer/O_C-Phazerville/wiki/Button2)** - 2 simple triggers or latching gates. Press the button!
* **[Calculate](https://github.com/djphazer/O_C-Phazerville/wiki/Calculate)** - Min, Max, Diff, Mean, Random, S&H
* **[Calibr8](https://github.com/djphazer/O_C-Phazerville/wiki/Calibr8)** - 2-channel, mini [Calibr8or](https://github.com/djphazer/O_C-Phazerville/wiki/Calibr8or) for v/Oct correction
* **[Carpeggio](https://github.com/djphazer/O_C-Phazerville/wiki/Carpeggio)** - X-Y table of pitches from a scale/chord
* **[Chordinate](https://github.com/djphazer/O_C-Phazerville/wiki/Chordinate)** - Quantizer with scale mask, outputs root + scale degree (from qiemem)
* **[ClockDivider](https://github.com/djphazer/O_C-Phazerville/wiki/ClockDivider)** - Dual complex clock pulse multiplier / divider.
* **[ClockSkip](https://github.com/djphazer/O_C-Phazerville/wiki/Clock-Skipper)** - Randomly skip pulses
* **[Compare](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Compare)** - basic comparator
* **[CVRec](https://github.com/djphazer/O_C-Phazerville/wiki/CV-Recorder)** - record / smooth / playback CV up to 384 steps on 2 tracks
* **[DivSeq](https://www.youtube.com/watch?v=J1OH-oomvMA)** - two sequences of clock dividers
* **[DrumMap](https://github.com/benirose/O_C-BenisphereSuite/wiki/DrumMap)** - clone of Mutable Instruments Grids
* **[DualTM](https://github.com/djphazer/O_C-BenisphereSuite/wiki/DualTM)** - highly configurable pair of Turing Machine shift registers (replacement for ShiftReg/TM)
* **[DualQuant](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Dual-Quantizer)** - basic quantizer
* **[Ebb & LFO](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Ebb-&-LFO)** - clone of Mutable Instruments Tides; oscillator / LFO with CV-controllable waveshape, slope, V/Oct, folding
* **[EnigmaJr](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Enigma,-Jr.)** - compact player of curated shift registers
* **[EnvFollow](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Envelope-Follower)** - follows or ducks based on incoming audio
  - added Speed control
* **[EuclidX](https://github.com/djphazer/O_C-BenisphereSuite/wiki/EuclidX)** - Euclidean pattern generator (replacement for [AnnularFusion](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Annular-Fusion-Euclidean-Drummer))
* **[GameOfLife](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Conways's-Game-of-Life-(Retired))** - experimental cellular automaton modulation source
* **[GateDelay](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Gate-Delay)** - simple gate delay
* **[GatedVCA](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Gated-VCA)** - simple VCA
* **LoFi Echo** - super crunchy PCM delay line, based on [LoFi Tape](https://github.com/Chysn/O_C-HemisphereSuite/wiki/LoFi-Tape)
* **[Logic](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Logic)** - AND / OR / XOR / NAND / NOR / XNOR
* **[LowerRenz](https://github.com/Chysn/O_C-HemisphereSuite/wiki/LowerRenz)** - orbiting particles
* **[Metronome](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Metronome)** - internal clock tempo control + multiplier output
* **[MIDI In](https://github.com/djphazer/O_C-BenisphereSuite/wiki/MIDI-Input)** - from USB to CV
* **[MIDI Out](https://github.com/Chysn/O_C-HemisphereSuite/wiki/MIDI-Out)** - from CV to USB
* **[MixerBal](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Mixer:Balance)** - basic mixer
* **[Palimpsest](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Palimpsest-Accent-Sequencer)** - accent sequencer
* **[Pigeons](https://github.com/djphazer/O_C-BenisphereSuite/wiki/Pigeons)** - dual Fibonacci-style melody generator
* **[PolyDiv](https://www.youtube.com/watch?v=J1OH-oomvMA)** - four concurrent clock dividers with assignable outputs
* **[ProbDiv](https://github.com/benirose/O_C-BenisphereSuite/wiki/ProbDiv)** - stochastic trigger generator
* **[ProbMeloD](https://github.com/benirose/O_C-BenisphereSuite/wiki/ProbMeloD)** - stochastic melody generator
* **[ResetClk](https://youtu.be/i1xU6-oPwfA)** - rapidly advance a sequencer to the desired step (from [pkyme](https://github.com/pkyme/O_C-HemisphereSuite/tree/reset-additions))
* **RndWalk** - clocked random walk CV generator (from [adegani](https://github.com/adegani/O_C-HemisphereSuite))
* **[RunglBook](https://github.com/Chysn/O_C-HemisphereSuite/wiki/RunglBook)** - chaotic shift-register modulation
* **[ScaleDuet](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Scale-Duet-Quantizer)** - 2 quantizers with independent scale masks
* **[Schmitt](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Schmitt-Trigger)** - hysteresis filter
* **[Scope](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Scope)** - tiny CV scope / voltmeter / BPM counter
  - expanded with X-Y view
* **[SequenceX](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Sequence5)** - up to 8 steps of CV, quantized to semitones
* **[ShiftGate](https://github.com/Chysn/O_C-HemisphereSuite/wiki/ShiftGate)** - dual shift register-based gate/trigger sequencer
* **[Shredder](https://github.com/benirose/O_C-BenisphereSuite/wiki/Shredder)** - clone of Mimetic Digitalis
* **[Shuffle](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Shuffle)** - it don't mean a thing if it ain't got that swing
  - triplets added on 2nd output
* **[Slew](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Slew)** - smooth things out
* **[Squanch](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Squanch---Shifting-Quantizer)** - advanced quantizer with transpose
* **[Stairs](https://github.com/Logarhythm1/O_C-HemisphereSuite/wiki/Stairs)** - stepped CV
* **[Switch](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Switch)** - CV switch
* **[TB-3PO](https://github.com/Logarhythm1/O_C-HemisphereSuite/wiki/TB-3PO)** - a brilliant 303-style sequencer
* **[TL Neuron](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Threshold-Logic-Neuron)** - clever logic gate
* **[Trending](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Trending)** - rising / falling / moving / steady / state change / value change
* **[TrigSeq](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Trigger-Sequencer)** - two 8-step trigger sequences
* **[TrigSeq16](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Trigger-Sequencer-16)** - one 16-step trigger sequence
* **[Tuner](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Tuner)** - oscillator frequency detector
* **[VectorEG](https://github.com/Chysn/O_C-HemisphereSuite/wiki/VectorEG)** - custom envelope shapes
* **[VectorLFO](https://github.com/Chysn/O_C-HemisphereSuite/wiki/VectorLFO)** - custom LFO shapes
* **[VectorMod](https://github.com/Chysn/O_C-HemisphereSuite/wiki/VectorMod)** - custom modulation
* **[VectorMorph](https://github.com/Chysn/O_C-HemisphereSuite/wiki/VectMorph)** - custom waveshaper tool
* **[Voltage](https://github.com/Chysn/O_C-HemisphereSuite/wiki/Voltage)** - static output CV