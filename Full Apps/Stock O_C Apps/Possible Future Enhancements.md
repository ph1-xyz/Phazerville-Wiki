Acid Curds
Automatonnetz
### CopierMaschine
 - the current ability to loop through the ring buffer of pitches encountered is half way to providing a more general "CV recorder" function - thus, either extend this app, or provide a seperate app, which can act as a general-purpose CV recorder, similar to the Shakmat Modular [Bishop's Miscellany](http://www.shakmatmodular.com/products.html) module, either with CV and gate recording on two channels, or just clocked CV recording on 4 channels.


 - portamento! Possibly with settable speeds in either direction, and a choice of curves and easing (spring physics portamento, perhaps?)
 - ~~adjustable sampling delay, as in Braids~~ (done!)
 - user-adjustable hysteresis parameters to fine-tune latency vs jitter for various scenarios and use-cases
 - are there any useful ideas or concepts in the [Barton User Writable Quantizer](http://www.bartonmusicalcircuits.com/uwq/documentation.pdf) that could be added to _Quantermain_?
 - a two-channel mode, in which two of the output channels, say A and C, emit quantised pitch CVs, and the other two channels, B and D, emit a corresponding gate or trigger, or even better, an envelope. This might be useful with trigger-less or non-clocked quantisation (that is, when `Trigger source` is set to `cont` (continuous)), and you want a trigger/gate/envelope to be output with the quantised pitch CV, each time the pitch changes to a different note. Settable delay and/or hysteresis is almost certainly required for such a feature to work reliably, or usefully.
 
Dialectic Ping-Pong
Harrington 1200
Low-rents
Meta-Q
Piqued
### Possible future enhancements 

 - ~~add a configurable delay (between receipt of trigger and start of attack segment of envelope) for each channel~~, ~~possibly externally CVable (done, but not currently under external CV control)~~ (done in v1.1)

 - add the ability to have the trigger delay take random values (with a settable range), so that there is varying "swing" - both uniform probability distribution within a range, and a Gaussian distribution of delay times around a mean.

 - add more envelope types with more segments (the Peaks envelope model is quite general and allows for an arbitrary number of segments per envelope).

 - add more envelope segment shapes, including a flat envelope with gradually increasing wiggles, for tremolo or vibrato. May need a DC offset setting as well so it could be centred around zero - that would be useful for other envelopes too, perhaps.

 - voltage-controlled envelope segment shape, perhaps? A bit clumsy, but might be interesting, and quite feasible. No change to UI needed, just a few more choices on the CV input mapping menu items.

 - add some of the features from the ADDAC505 Mille Plateaux module, in particular: sustain time (i.e. internally generated gate duration - what a great idea!), and non-zero start and end amplitudes for each segment (also a great idea).

 - ~~add some trigger processors, such as a Euclidean pattern generator, so that a regular clock/trigger input signal can be "filtered" into a rhythmic pattern of generated envelopes.~~ - done!

 - add "anti-Euclidean" (i.e. Golomb ruler) and "divided" Euclidean patterns as shown in [this video](https://www.youtube.com/watch?v=_h7bInSc4h4) about the Shakmat Knight's Gallop module.
Quadraturia
Quantermain
References
Scenes
Sequins
Viznutcracker
### Possible future enhancements 
 - add more byte beat equations (16 more added in v1.1!)
 - investigate whether smoothing of the byte beat value stream is useful when they are used a modulation sources
 - investigate whether digital filtering of the byte beat audio stream is feasible, or useful


