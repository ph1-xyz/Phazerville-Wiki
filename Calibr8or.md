### Quad Performance Quantizer + Pitch Fine-Tuning App
Based on a design spec from Chris Meyer ([Alias Zone](https://aliaszone.com/) / [Learning Modular](https://learningmodular.com/)) - this is a **4-channel Pitch CV fine-tuning tool** with performance-oriented transpose controls. Each channel can be clocked for latching of the _Transpose_ value or full S&H of the input. There are 4 preset banks to store and quickly switch configurations.

The Fine Tune controls at the bottom of the main view apply voltage _Scaling_ and _Bias Offset_ to the output stage, per channel. Scaling is in increments of ±0.01% and Bias is effectively ±1/128th of a semitone.

There's a mini applet version called _Calibr8_. Paired with the Tuner applet, this is can be handy for examining the pitch-tracking of your oscillators! Accurate performance will depend on the calibration of your o_C module itself.

### Calibr8or Controls:
- UP / DOWN buttons - switch channels
- Long-press Left Encoder - cycle Clocked Transpose / S&H modes per channel
- Quick-press Left Encoder - switch between Transpose and Fine-Tune controls
- Quick-press Right Encoder - toggle Scale & Root Note selection
- Long-press DOWN button - preset switching
  - turn or press Left Encoder to toggle Save/Load
  - use Right Encoder to select
  - UP or DOWN to cancel
- Dual-press UP+DOWN for Clock Setup (shared with Hemispheres)

Note: the presets are not stored in EEPROM unless you save the module state (with a Right Encoder Long-press, twice)