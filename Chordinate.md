Chordinate is a quantizer with scale mask, outputting a root note pitch and a scale degree offset (from [qiemem](https://github.com/qiemem/O_C-HemisphereSuite)). The scale mask allows only user-determined intervals relative to the root note to be a valid output on CV 2/4.

### I/O

|                |              1/3           |                   2/4                |
| -------------- |:---------------------------:|:-------------------------------------:|
| Trig (Digital) |  Sample & hold root note (CV 1)   | Sample & hold scale degree (CV2) |
| CV In          | Root note pitch input |      Scale degree offset weight     |
| Output         |        Root note pitch (thru)           |         Scale degree pitch          |

_Note that sending a trigger to either digital input will initiate a clocked S&H mode, which will persist until power cycling. Root note and scale degree may be held independently, allowing for syncopated voicing changes_

### UI Parameters
* Quantizer scale
* Root note 
* Scale mask