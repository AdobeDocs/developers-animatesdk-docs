## timeline.clearFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.clearFrames(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

**startFrameIndex** A zero-based index that defines the beginning of the range of frames to clear. If you omit
>
*startFrameIndex*, the method uses the current selection. This parameter is optional.
>
**endFrameIndex** A zero-based index that defines the end of the range of frames to clear. The range goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the value of *startFrameIndex*. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; deletes all the contents from a frame or range of frames on the current layer.

#### Example

```
The following example clears the frames from Frame 6 up to, but not including, Frame 11 (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().clearFrames(5, 10); The following example clears Frame 15: fl.getDocumentDOM().getTimeline().clearFrames(14);

```