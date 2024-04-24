### Harrington 1200

Try using a rhythm generator, such as the Mutable Instruments [Grids](http://mutable-instruments.net/modules/grids) module, or the ALM/Busy Circuits [Pamela's Workout](http://busycircuits.com/alm001/) module, or the Rebel Technology [Stoicheia](http://www.rebeltech.org/products/stoicheia/) module, or some combination of clock division and logic modules, or even a second O+C module running the _Piqued_ app with Euclidean trigger filters engaged, to trigger the P, L and R transformations (via trigger inputs TR2, TR3 and TR4) in varying patterns to create a variety of chord progressions that may or may not be musically pleasing, or interesting, or horrifying.
### Quadraturia
- To achieve the classic quadrature LFO patch (incremental 90° phase offset on outputs), set the phase/frq spread to +127.
    
- Try mixing the some of the outputs with a DC-coupled mixer (such as the Mutable Instruments Shades or Links modules) in order to create even more complex waveforms.
### Quantermain
You can disable quantisation on each channel by setting the scale to `Off`. When in clocked mode (that is, `Trigger source` is set to TR1, TR2, TR3 or TR4), then that channel acts as a traditional sample-and-hold (S&H), without any voltage droop, of course. Thus, Quantermain can act as a quad S&H if you want. The only limitation is that the effective maximum sample rate is about 1 kHz, even if the clock/trigger signal you give it is at a higher frequency. This is because the ADCs are only read at an effective rate of about 1 kHz.

Disabling quantisation when using a Turing Machine or Logistic map as a source allows the output for that channel to act as a semi-random modulation source.
### Sequins
- if identical sequences are set up on both sequencer channels, and the same clock input is used to drive both channels, then [Steve Reich “Piano Phase”](https://en.wikipedia.org/wiki/Piano_Phase) type effcts can be acheived by setting the `mult/div` setting for one channel to, say, `/32` (divide by 32), and to `/31` on the other channel, and then using a fast clock. The two sequences will slowly move out of phase. By varying the division up and done in one channel, the two sequences can be moved in and out of phase as required.
- If you set the `aux. mode` to one of the envelope types (as an alternative to just gate or trigger out), then an additional setting `--> loops` will appear in the menu. This setting defaults to 1, but you can increase that, and then each time the envelope triggers, it will loop that set number of times. Tthat gives you a fixed ratchet-like effect, which might be useful in some circumstances.
    - However, in the CV assignment menu (see above), you can assign an input CV to the loops parameter using the `env loops ->` setting. If you do that, and also set `--> loops` to 1 in the main menu and you can then use an external voltage (which could be a gate signal, suitably attenuated) to vary the number of loops for each new step in the sequence between 1 and 127 (usually you would want between 1 and 3 or 4). Of course, the voltage to do that can come from the other channel of Sequins, so you can set the number of envelope loops at each step in channel A by a sequence in channel B, clocked from the same source, and cross-patched to one of the CV inputs configured to affect the loops parameter for channel A. Or you can use external voltages, of course, including controllers such as joysticks etc.
    - You can do something similar in the Piqued app, because there is a Loops parameter for the looping envelope types, and you can put that under external CV control.
### Lowrents
If you have an oscilloscope capable of displaying X/Y (vectorscope) signals, try patching pairs of the _x_, _y_ and _z_ outputs from either type of generator into it to observe the classic strange attractor patterns.
### Vitznutcracker, Sweet!
  - as noted above, use the byte beat generators at very slow rates to generate DC control voltages. Feed these to a quantiser to produced pitch sequences, or pass them through a portamento or slew-limiting module to create interesting smooth modulation signals, or use them as-is, to modulate filters etc.
 
  - process the byte beats outputs running at audio rates through a low-pass or shelf filter to remove some of the high-pitched screech
  
  - process the output through band-pass filters (such as the [Mutable Instruments Shelves](http://mutable-instruments.net/modules/shelves) filter), or other complex filtering arrangements subject to slow modulation (by another O+C module, perhaps)
  
  - process the output through a VCA and/or filter with a percussive envelope to produce interesting, well, percussive sounds. Use the same trigger or gate signal used to fire the envelopes also reset the phase on the byte beat generator. Use slow modulation to slowly vary the frequency/rate, and/or to "scrub" loop start and end points in order to vary the nature of the percussive sound.