[![Stolen Ornaments: Pigeons](http://img.youtube.com/vi/J1OH-oomvMA/0.jpg)](http://www.youtube.com/watch?v=J1OH-oomvMA "Stolen Ornaments: Pigeons, PolyDiv & DivSeq | O_C Phazerville Suite")

## What is the Pigeonhole Principle?
The core concept is related to the Fibonacci Sequence, based on [**this most excellent video**](https://www.youtube.com/watch?v=_aIf4WUCNZU) by Marc Evanstein. Something about the way numbers behave in modular arithmetic being akin to a limited number of pigeonholes for an infinite number of pigeons...

## How does the applet work?
This applet generates two Pitch CV values at the Outputs, quantized using a given Scale and Root Note.

There are two **Pigeons** (channels), independently triggered. They are each singing a _note_ (a number representing scale degree) and have a certain number of holes they can visit (the _modulus_). When triggered, each one adds the current and previous _notes_ together, divides by the _modulus_ value, and uses the remainder for the next _note_. The pair of notes represents the coordinates of the current hole; your Pigeon is guaranteed to revisit the same holes eventually.

Pigeons are easily triggered - by the physical trigger inputs, internal clock pulses, or neighboring trigger sequencer applets (like [ProbDiv](https://github.com/benirose/O_C-BenisphereSuite/wiki/ProbDiv)).

The **CV inputs** change the _modulus_ value for each channel, affecting the range of the generated melodic sequence. It is possible to cause both note values to drop to 0 (the root note), and your Pigeon will take a nap there. If that happens, you'll have to nudge it with the encoder, or maybe load a Preset with a MIDI PC message...