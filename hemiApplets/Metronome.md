Metronome is a control system for the [Hemisphere internal clock](https://github.com/Chysn/O_C-HemisphereSuite/wiki/_Hemisphere-Basic-Instructions#5-internal-clock)

Controls
* CV Outs: Out 1 sends a clock pulse on the specified multiples of the beat, and Out 2 sends a clock pulse on each beat.
* Encoder: Sets the tempo of the internal clock

The internal clock provides a way to use Hemisphere's sequencers and other clocked applets without an external clock source. A Clock Setup screen allows changes to tempo and clock multiplier.

To access the Clock Setup screen, long-hold the Down control button for about two seconds. When you release it, the Clock Setup screen will appear. Use either encoder button to move the cursor between the clock source, tempo (in beats per minute), and multiplier (from x 1 to x 24). Turn either encoder to change the value at the cursor. Push either the Up or Down control button to return to Hemisphere's main screen.

If the clock source is set to Internal, you'll see a small metronome icon on the main screen. To start or stop the clock, long-hold the left encoder button. The clock will start or stop when you release the button. While the internal clock is running, any digital input that expects a "clock" signal will respond as though a clock signal is present at the jack.

Metronome is in Hemisphere Suite starting at v1.6.