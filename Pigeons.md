This applet generates two Pitch CV values at the Outputs, quantized using a given Scale and Root Note. The core mathematical concept is related to the Fibonacci Sequence, based on [this most excellent video](https://www.youtube.com/watch?v=_aIf4WUCNZU).

There are two **Pigeons** (channels). They are each singing a _note_ (a number representing scale degree) and - when triggered - one adds it to the previous _note_, divides by a _number_, and uses the remainder for the next _note_.

Pigeons are easily triggered - by the physical trigger inputs, internal clock pulses, or neighboring applets that generate triggers (like [ProbDiv](https://github.com/benirose/O_C-BenisphereSuite/wiki/ProbDiv)).

The CV inputs change the _modulo_ number for each channel, affecting the range of the generated melodic sequence.