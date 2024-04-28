# Ornaments & Crimes v1.1.x: Extended Firmware for the Ornament & Crime DIY eurorack module

The documentation on this page refers to v1.1.x firmware for Ornament & Crime. **The most recent version of the firmware is v1.2 and documentation for it can be found [here](http://ornament-and-cri.me/user-manual/).**

![welcome](https://c1.staticflickr.com/9/8081/29067972953_84e42ba7ac_k.jpg)

- **Ornaments & Crimes** is a collaborative [open-source](https://github.com/mxmxmx/O_C/wiki/Licensing-of-Ornament(s)---and-Crime(s)) project by Patrick Dowling (aka pld), mxmxmx and Tim Churches (aka bennelong.bicyclist). It (considerably) extends the original firmware for the Ornament & Crime (O+C) DIY eurorack module, designed by mxmxmx. 

- There is still a **quantising ASR** (analogue shift register) function in Ornaments & Crimes, now named _CopierMaschine_, **but several other "apps" have been added**. These apps are selectable **on-the-fly**, without having to reboot the module or toggle the power. Several of these apps are experimental, or perhaps, quirky, in nature, which is not an accident: O+C makes an ideal platform for (relatively) quickly prototyping of ideas and testing them in the eurorack modular synth context. That said, none of the apps are intended to be just toys, and some provide cutting-edge performance and/or capabilities not currently found in any other eurorack module. 

- The O+C module, and the Ornaments & Crimes firmware for it, also break new ground as a **polymorphic module**: a generic set of inputs and outputs are provided, and the textual OLED display is used to permit re-mapping of these inputs and outputs for each app, and in some cases, for each of the four channels within each app. Further refinement of this polymorphic design pattern is planned. Hard-wired, analogue modules are necessarily single-purpose, but the same is not true of digital modules, in the same way that (say) a modern smartphone can be used for a great deal more than just telephony. We believe that a single, somewhat generic module can serve as an adequate platform for many different purposes and functions. The O+C module does not purport to be the paradigmatic pinnacle of polymorphism - in fact, it was originally designed to fulfil just one purpose (= ASR) - but together with the Ornaments & Crimes firmware suite for it, we hope it provides an interesting and useful early step in the evolution of such multi-purpose modules. 

- The TL;DR version of this documentation: _**qual**_, in Seattle, has kindly assembled a very useful "cheat sheet" containing a condensed version of this documentation, available [here](https://docs.google.com/spreadsheets/d/166WdC7MtESS56JNyDNtMUKI--PVipZwUJiWq2_fFDDk/edit#gid=0).

#####The apps currently available in Ornaments & Crimes are:

- [_CopierMaschine_](#copiermaschine) is an enhanced version of the original quantising digital emulation of a four stage analogue shift register (ASR).
- [_Harrington 1200_](#harrington-1200) provides basic neo-Riemannian Tonnetz transformations of triadic chords, triggered by the digital (gate/trigger) inputs.
- [_Automatonnetz_](#automatonnetz) combines Tonnetz transforms with a "vector" sequencer - it can be both a chord sequencer and a melody sequencer, but not of the usual kind.
- [_Quantermain_](#quantermain) is a quad pitch quantiser for external voltages, with editable scales; it can do clocked (trigger-driven) quantising, or continuous quantising, with a latency of under 100 microseconds; it also features quad Turing Machines, May-Verhulst logistic maps or byte beats as optional, semi-random, internally generated CV sources.
- [_Quadraturia_](#quadraturia) is a wavetable quadrature LFO, based on the "Easter egg" in the [Mutable Instruments Frames](http://mutable-instruments.net/modules/frames) module.
- [_Low-rents_](#low-rents) is a dual Lorenz and Rössler (strange attractor) modulation generator, partially based on the "Easter egg" in the [Mutable Instruments Streams](http://mutable-instruments.net/modules/streams) module.
- [_Piqued_](#piqued) is a quad voltage-controlled envelope generator, based on envelope generator code from the [Mutable Instruments Peaks](http://mutable-instruments.net/modules/peaks) module, but extending it with voltage control, additional envelope types, including re-triggering (looping) envelopes, additional segment shapes, adjustable trigger delays, and a unique Euclidean "trigger filter" which turns the app into a Euclidean rhythm generator which can output envelopes, not just gate or trigger pulses.
- [_Dialectic Ping Pong_](#dialectic-ping-pong) is a quad bouncing ball envelope generator, based on a hidden mode of the [Mutable Instruments Peaks](http://mutable-instruments.net/modules/peaks) module.
- [_Viznutcracker, sweet!_](#viznutcracker-sweet) is a quad "byte beat" equation generator, which can be used as an audio source to generate curious but often interesting 8-bit noises and tunes, or which can be clocked by an external source to produce "byte beat" control voltage sequences. "Byte beats" were first [described](http://countercomplex.blogspot.com/2011/10/algorithmic-symphonies-from-one-line-of.html) in 2011 by viznut (aka Ville-Matias Heikkilä). 
- [_References_](#references) is a simple utility app that outputs specific reference voltages on each channel to help tune or calibrate VCOs and other modules.

For information about the O+C module **hardware**, including DIY build details, please start [here](https://github.com/mxmxmx/O_C/wiki/hardware-basics).

### Appendices
 - [VIDEOS](https://github.com/mxmxmx/O_C/wiki/Ornament-and-Crime-videos-and-tracks)
 - [CHANGELOG](#changelog)
 - [credits, thanks, acknowledgements, and sources of inspiration](#credits-thanks-acknowledgements-and-sources-of-inspiration)
 - [licensing of PCB design files and of firmware and its source code](https://github.com/mxmxmx/O_C/wiki/Licensing-of-Ornament(s)---and-Crime(s))
 - [known issues and things to be checked and improved](#known-issues-and-things-to-be-checked-or-improved)
 - [implementation notes](Implementation-Notes) regarding the Ornament + Crime module hardware and the Ornaments & Crimes firmware
 - the [poem-mascot](https://web.cs.dal.ca/~johnston/poetry/pitmonster.html) for this module and its firmware
 - Gedanken Affe, the [organism-mascot](https://scontent-sjc2-1.xx.fbcdn.net/v/t1.0-9/14344712_10211125934092188_7011003688783017761_n.jpg?oh=a17a4d1ac1978fda1f65c558e62069df&oe=587D09E8) for this module and its firmware

## Startup

Immediately after power-on, the start-up phase is indicated by a line at the bottom of the display which progressively shrinks right-to-left. By default, following start-up phase, the module boots into the last saved app, unless one of the encoders is held down:
- hold down the Left encoder: Boot into calibration mode (unchanged from the original O+C firmware - please see the calibration procedure [here](https://github.com/mxmxmx/O_C/wiki/calibration))
- hold down the Right encoder: Enter the app selection menu

## App Selection
The **app selection menu** can be reached either when the module is first powered on, as described above, or by depressing the right encoder for two seconds or longer (a long press) during normal use.

- Turn the right encoder to select an app
- Press the right encoder to switch to the selected app
- Pressing the Up button (the upper button to the right of the display) while the App Selection screen is displayed toggles encoder acceleration on and off (there is no visual indication of this). Encoder acceleration increases the amount by which values are incremented or decremented on each encoder rotational click when you are rapidly spinning the encoder in value edit mode, rather than advancing it slowly one click at a time. This speeds up sweeping across the full range of values, while still retaining full precision when moving the encoder one step at a time.

## Save Settings / Module State
Settings aren't saved automagically. To save the current state/settings, enter the **app selection menu** (see above), then **long press** the right encoder (>2s) **again** to save the module state and make the selected app the default at the next boot. This also saves all the current settings of **all apps**.

- The settings are saved permanently in the Teensy EEPROM storage. (The settings storage uses a basic form of wear-levelling. EEPROM memory can only be written to a certain number of times before it becomes unreliable. The EEPROM storage on the Teensy 3.2 used in O+C is good for at least 100,000 write cycles, and probably a lot more. Meaning, you are very unlikely to wear out the EEPROM memory in the Teensy processor in your O+C module with normal use.)

## General operation of the apps

Each app has two display pages, a settings mode and a "screensaver" mode. The apps drop into screensaver mode after a short period of inactivity (that is, no user interaction); the timeout period can be set in the [calibration menu](https://github.com/mxmxmx/O_C/wiki/calibration#4-screensaver-timeout-period). Alternatively, **long press** (> ~ 1.5 sec) the `up button` to **preview** the screensaver. 

- In the background, the module functions the same regardless of whether settings are displayed or the screensaver is displayed. When the screensaver is displayed, clicking or rotating either of the two encoders, or pressing the Up or Down buttons will immediately swap to the settings display.

- In settings mode, for most of the apps, the right encoder is used to scroll up and down the list of available settings, and clicking on the right encoder will toggle edit mode, indicated by one or two small up/down triangles next to the setting. Turning the right encoder when in edit mode will increment (increase) or decrement (decrease) the relevant setting. Clicking again on the right encoder toggles back to settings selection mode.

- In multi-channel apps, the left encoder selects which of the four channel (A to D) settings are currently displayed (and editable). All channels remain active in the background, all the time, even while editing settings. The channel can be changed even when value edit mode is active, making it easy to edit the same setting on each ofthe four channels. 

- In other apps, the left encoder is used to set a root note or a transposition, or to set frequency or rate. Its exact behaviour is noted below in the documentation for each of the apps.

- The two buttons to the right of the display (the Up and Down buttons) either transpose notes up or down an octave, or increase or decrease frequency or speed in steps of 32 (with a few exceptions for some apps, as noted below). 

***

[[Full Apps/Stock O_C Apps/CopierMaschine]]

***
[[Full Apps/Stock O_C Apps/Harrington 1200]]

***
[[Full Apps/Stock O_C Apps/Automatonnetz]]

***
[[Full Apps/Stock O_C Apps/Quantermain]]

***
[[Full Apps/Stock O_C Apps/Quadraturia]]

***
[[Full Apps/Stock O_C Apps/Low-rents]]

***
[[Full Apps/Stock O_C Apps/Piqued]]

***
[[Full Apps/Stock O_C Apps/Dialectic Ping-Pong]]

***
[[Full Apps/Stock O_C Apps/Viznutcracker, sweet!]]

***
[[Full Apps/Stock O_C Apps/References]]

***

# CHANGELOG

## Changes between v1.0 and v1.1

* removal of some redundant code and unused libraries
* changes to the encoder direction setting when in calibration mode to accomodate the swap in GPIO pin assignment for the right encoder introduced in version 2c and later of the O&C PCBs - see [setting encoder directions](https://github.com/mxmxmx/O_C/wiki/calibration#0-setting-encoder-directions) on the calibration wiki page.
 
* _Quantermain_
  * mappable input CV sources to control the built-in LFSR (Turing Machine) probability and range parameters have been added - yes, voltage-controlled Turing Machines!
  * mappable CV input sources to control the built-in Logistic Map R and range parameters have been added, so now the Logistic Map can also be voltage-controlled.
  * byte beat equations have been added as a third internal source for the quantiser, with a range of parameters that can be voltage controlled. Thus, rather than creating audio output using byte beats (which is still possible using the _Viznutcracker, sweet!_ app), uniquely, the Quantermain app can create four independent channels of quantised pitch voltage streams driven by clocked byte beat equations. We believe this is a completely novel application of byte beat equations, and one which produces surprisingly musically interesting results ([here is an example](https://soundcloud.com/bennelong-bicyclist/equitable-equations)).

* _Quadraturia_
  * a frequency range parameter for the quadrature LFOs has been added, with self-explanatory settings of "vslow", "slow", "med", "fast" and "vfast". The faster settings extend into audio range. Note that Quadraturia does not, and is not intended to, track 1V/octave.
  * output amplitude parameters for each channel have been removed (they weren't much use, it could be done in an external mixer anyway, and they wasted precious settings storage space).

* _Piqued_ 
  * voltage control over the Euclidean trigger filter parameters and the trigger delay time is now possible. Input CVs can be mapped to control the Euclidean trigger filter parameters: Eleng (Euclidean pattern length), Efill (Euclidean pattern fill, Eoffs (Euclidean pattern offset/rotation), or the trigger delay time (Delay).
  * added an new envelope type: Gate. This can be used when gate outputs are desired. The value rises immediately to maximum in the attack segment, and the value falls immediately to minimum in the decay and release segments. In other words, a gate pulse is output.

* _Viznutcracker, sweet!_
  * eight new byte beat equations have been added, bringing the total to 16. These new equations are also available as sources in the _Quantermain_ quantiser app (see above).
 
***

[[Full Apps/Stock O_C Apps/zz_Credits, thanks, acknowledgements, and sources of inspiration]]
 
***

# Known Issues and Things to be checked or improved
- the 16.6 kHz DAC update rate means that audible digital aliasing is present when the output is used as an audio source - which is why the only app intended as an audio source is _Viznutcracker, sweet!_, which, as a byte beat generator, **depends** on lots of horrible digital aliasing and related digital artefacts to create its distinct sound. That said, several of the other apps can produce signals in the audio range, but you may need to use them with a low-pass filter to remove some of the aliasing noise (if you wish - some people like the inharmonic "sizzle" of digital aliasing). Anyway, just be aware that O+C is intended to be used as a pitch CV generator, and as a slow modulation CV source, not as audio oscillator or audio signal generator. In theory, some of the digital aliasing may "bleed through" into the audio domain even when the O+C is used as a modulation CV source (eg as an envelope generator or LFO modulating a VCF cut-off or VCA gain). We have not found that to be a problem in practice, but if it does become apparent, then you can always interpose a low-pass filter between the O+C and whatever is being modulated. WMD make a module exactly for this purpose: the [Quad Anti-aliasing Filter (QAAF)](https://www.wmdevices.com/collections/eurorack-modules/products/quad-anti-aliasing-filter-qaaf). However, this is unlikely to be required. Note that for its original designed purpose, as a module that deals with or generates pitch CVs, the 16.6 KHz DAC update rate is not a problem.
- when used as an LFO (that is, the _Quadrature_ app), the waveform is not symmetrically bipolar, because the output range of the module is -3V to +6V. This can be corrected by adding -1.5V to each output, so that the output range is shifted from -3V to 6V, to -4.5V to +4.5V. The [Mutable Instruments Shades](http://mutable-instruments.net/modules/shades) module is excellent for doing such level shifting (and voltage scaling), but there are many other utility modules which can do the same. The Lorenz and Rössler functions output by the _Low-rents_ app are similarly asymmetrical - they also range from -3V to + +6V, due to the hardware design of O+C.
- ~~note names and input/output voltage may not match in Harrington 1200/Automatonnetz modes~~ => fixed!
- ~~root quantization and output not verified yet~~ => verified!
- ~~No chromatic scale in quantizer mode (see [roadmap](#roadmap))~~
- More flexible quantiser implementation in 4x mode
 - ~~SCALA-style scale definitions~~ => using Braids' quantizer
 - ~~Check hysteresis/ADC jitter since I've been able to find settings where it's "stuck" between two steps in cont mode~~ => internally ADC sampling/smoothing improved, seems good enough
 - bit-mask or other way to choose which notes in scale are active
 - ~~(meaningful) linking of channels and/or offsets?~~ => Source CV is selectable, original source is used as transpose
- extend tonnetz to support other chord modes (augmented, diminished) and maybe more transforms?
- CV control of dx/dy and other parameters in _Automatonnetz_
- a note grid sequencer app
- a quad free-running LFO app, possibly implementing some of the features of the [Modcan Quad LFO](http://www.modcan.com/emodules/quadlfo.html) module.
- port some of the clock and gate/trigger logic capabilities of the [_temps utile_](https://github.com/mxmxmx/temps_utile-/wiki/Temps-Utile) module to O+C. The functionality of the [Bastl Little Nerd](https://www.youtube.com/watch?&v=zYJJLJF9l4A) module could also be replicated, although with only 4 outputs, but 4 independent clock inputs, instead of just 2. The [Malekko Varigate](https://www.voltagecontrollab.com/2015/12/28/malekko-varigate-4/) is also worthy of study.
- (per loopt on MW): "_For the piqued app you could implement an additional 281-mode with two AD envelopes and two of the CV outputs spitting out gates (EOR of AD1 and EOD of AD2)...Any plans of implementing more env stages with loops?_
_Or some gate logic for conditional looping, as in Gate 1 AND Gate 3 are high -> loop Env2._"
- The ideas behind XronoMorph might make for an interesting generative rhythm/melody sequencer? See http://www.synthtopia.com/content/2016/04/27/free-app-for-os-x-windows-xronomorph-lets-you-explore-new-theory-of-rhythm/

***


o_C is a collaborative project by Patrick Dowling (aka pld), mxmxmx and Tim Churches (aka bennelong.bicyclist) (though mostly by pld and bennelong.bicyclist). it (considerably) extends the original firmware for the o_C / ASR eurorack module, designed by mxmxmx.