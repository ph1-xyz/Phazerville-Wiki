## Credits (who did what)

We welcome contributions from others (ideally via _pull_ requests on GitHub) to the Ornaments & Crimes firmware, and we will acknowledge any such contributions in detail. To make such detailed acknowledgements easier, we have documented here the contributions of the original developers of O+C and the Ornaments & Crimes firmware. If you make a contribution which is included the firmware, we'll add your name! 

### Hardware

- Max Stadler (aka mxmxmx): 
  - all hardware and circuit design
  - PCB layout
  - hardware debugging
  - build and calibration instructions and procedures

### Firmware
- Max Stadler: 
  - overall firmware framework and hardware interfacing abstractions
  - original menu system design (still used) and calibration procedures
  - original ASR and quantiser code, which became the _CopierMaschine_ app
  - lots of testing, debugging, and tweaking of code

- Patrick Dowling (aka pld)
  - design and implementation of loadable "apps" framework
  - conversion to interrupt and event-driven operation
  - writing of super-fast double-buffered DMA custom OLED display driver
  - design and implementation of the scale editor used in the _CopierMaschine_ and _Quantermain_ apps, and the porting of the Mutable Instruments Braids note quantiser code
  - creation of an enhanced menu framework
  - porting of original ASR code by Max Stadler to the _CopierMaschine_ app
  - the debugging displays
  - design and implementation of the _Harrington 1200_ app, including the neo-Riemannian tonnetz transformation classes
  - design and implementation of the _Automatonnetz_ vector sequencer app
  - design and implementation of the _Quantermain_ quad quantiser app, based on the _CopierMaschine_ app, and including implementation of Turing machine internal source for it
  - design and implementation of the _Quadraturia_ app, including porting the Mutable Instruments Frames Easter egg quadrature LFO code, and design and implementation of the waveform preview display
  - design and implementation of the _Piqued_ app, including porting of the Mutable Instruments Peaks envelope generator code and creation of the very nifty envelope visualisation display 
  - lots of the end user and system documentation
  - lots of tweaks and improvements to the ham-fisted code written by Tim Churches 
  - lots of testing, debugging, and tweaking of other code

- Tim Churches (aka bennelong.bicyclist):
  - design and implementation of the _Low-rents_ app, including porting of the Mutable Instruments Stream Easter egg Lorenz attractor code, and addition of Rössler attractor
  - design and implementation of the _Dialectic Ping Pong_ app, including porting of the bouncing ball physics simulation from the Mutable Instruments Peaks source code
  - design and implementation of the _Viznutcracker, sweet!_ byte beats app, including the curation and porting of byte beats equations from various sources (see app documentation above for acknowledgement of those sources).
  - suggesting the Harrington 1200 app and naming it, and design of the "circle of fifths" chord display using in its screensaver (and in the Automatonnetz screensaver)
  - suggesting that the fcd72 vector sequencer might be used, somehow or other
  - addition of May-Verhulst logistic maps as an internal source for the _Quantermain_ app
  - naming of the _Quadraturia_ app, and addition of frequency division and XOR capabilities to it
  - addition of trigger delays and Euclidean pattern filters to _Piqued_
  - addition of settable and additional segment shapes to the _Piqued_ app
  - quite a lot of this documentation
  - lots of testing, debugging, and tweaking of code

## Thanks
 - Enormous thanks to Olivier Gillet of Mutable Instruments for all of the wonderful [open-source module code](https://github.com/pichenettes/eurorack) which we have ported to and re-used in O+C 
 - Paul Stoffregen for creating the open-source [Teensy platform](https://www.pjrc.com/teensy/teensy31.html) and associated firmware libraries used by the O+C module
 - Bret Truchan for permission to use byte beats equations which he collected, devised  and curated for the excellent Microbe Modular [Equation Composer](http://microbemodular.com/products/equation-composer/overview) module, which is highly recommended for anyone interested in byte beats
 - Stephen from Noise Engineering for helpful notes and info about the neo-Riemannian transformation implementation in his [Tonnetz Sequent](http://www.noiseengineering.us/tonnetz-sequent/) module, which is highly recommended for anyone interested in tonnetz harmonies.
 
## Acknowledgements and sources of inspiration
 - the Noise Engineering [Tonnetz Sequent](http://www.noiseengineering.us/tonnetz-sequent/) module for introducing us to [neo-Riemannian transformations](https://en.wikipedia.org/wiki/Neo-Riemannian_theory) and harmonic tonnetz music theory
 - Frank Daniels (aka fcd72) for many of the [ideas behind the vector sequencer](https://dmachinery.wordpress.com/2013/01/05/the-vector-sequencer/) used in the _Automatonnetz_ app
 - the [KlangbauKöln RND – Logistische Gleichung](http://www.klangbauköln.de/klangbau-in-koeln/rnd-modul-logistische-gleichung/) module and the alternative (expert) firmware for the [XAOC Batumi](http://xaocdevices.com/main/batumi/) module for introducing us to the use of [May-Verhulst logistic maps](https://en.wikipedia.org/wiki/Logistic_map) as a semi-random value source.
 - Hal Chamberlin (author of the excellent book “Musical Applications of Microprocessors”), Grant Richter (designer of the [Wiard NoiseRing](http://mamonu.weebly.com/wiard-noisering.html) module) and Tom Whitwell (designer of the popular [Music Thing Turing Machine](http://musicthing.co.uk/modular/?page_id=21) module) for the LFSR/Turing Machine ideas - see [this reading list](http://musicthing.co.uk/modular/wp-content/uploads/2012/05/Random-Reading-List.pdf) assembled by Tom Whitwell for an introduction to the musical uses of LFSRs.
 - viznut (aka Ville-Matias Heikkilä) for discovering and [describing](http://countercomplex.blogspot.com/2011/10/algorithmic-symphonies-from-one-line-of.html) "byte beats"in 2011. 

