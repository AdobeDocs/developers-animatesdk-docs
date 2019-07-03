## timeline.convertToBlankKeyframes()

#### Availability

Flash MX 2004.

#### Usage

timeline.convertToBlankKeyframes(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

**startFrameIndex** A zero-based index that specifies the starting frame to convert to keyframes. If you omit
*startFrameIndex*, the method converts the currently selected frames. This parameter is optional.
**endFrameIndex** A zero-based index that specifies the frame at which the conversion to keyframes will stop. The range of frames to convert goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the value of *startFrameIndex*. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; converts frames to blank keyframes on the current layer.

#### Example

```
The following example converts Frame 2 up to, but not including, Frame 10 to blank keyframes (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().convertToBlankKeyframes(1, 9); The following example converts Frame 5 to a blank keyframe: fl.getDocumentDOM().getTimeline().convertToBlankKeyframes(4);

```