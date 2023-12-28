[Long-press DOWN button] to access.

### Presets
The first two options are **Load** and **Save**. Rotate either encoder to select, push to start. Press UP or DOWN buttons to cancel. Both applets (plus Clock Setup) with their state are recalled, along with the rest of the Config options on this page.

#### **Auto-save** - New in v1.6.999
If enabled, settings are automatically stored in the last loaded Preset when the screensaver is invoked, or when loading the main App menu via Right Encoder Long-press. (You can set the screensaver timeout as low as 1 minute in Calibration)

As of v1.6.999, when storing a Preset, settings are immediately written to EEPROM - no more need to manually do an EEPROM Save! Combined with Auto-save, this can result in frequent EEPROM writes... (only 100,000 write cycles are guaranteed, so use at your own risk!)

### Trigger Length
This sets the pulse width (in milliseconds, approximate) for applets that generate simple triggers, such as **EuclidX** or **TrigSeq**. The old default was close to 3ms, but some modules may require longer pulses.

### Screensaver
New in v1.6.999 - options are "[blank]", "Meters", "Zaps" and "Zips" (or "Stars" in Teensy 4.x builds)

### Cursor Edit Mode
The default cursor style is **modal** - rotate to move cursor, push to toggle editing, rotate to edit, push to toggle editing.

Here, you can select whether the cursor will **wrap** around or not when moving it, as well as the **Legacy** mode which behaves like original Hemisphere - push to advance, rotate to edit.

## Future

I want to stick a few more settings in here, on extra pages... which is menu-divey, unfortunately, but could be useful I think? Things like 4 global Quantizer settings, maybe I/O routing, MIDI stuff.