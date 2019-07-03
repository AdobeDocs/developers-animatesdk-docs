## frame.startFrame

#### Availability

Flash MX 2004.

#### Usage

frame.startFrame

#### Description

Read-only property; the index of the first frame in a sequence.

#### Example

```
In the following example, stFrame is the index of the first frame in the frame sequence. In this example, a frame sequence is spanning the six frames from Frame 5 to Frame 10. Therefore, the value of stFrame at any frame between Frame 5 and Frame 10 is 4 (remember that index values are different from frame number values).
var stFrame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[4\].startFrame; fl.trace(stFrame); // 4
var stFrame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[9\].startFrame; fl.trace(stFrame); // 4

```