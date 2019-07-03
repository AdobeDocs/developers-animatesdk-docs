## timeline.reverseFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.reverseFrames(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

**startFrameIndex** A zero-based index that specifies the first frame at which to start reversing frames. If you omit
>
*startFrameIndex*, the method uses the current selection. This parameter is optional.
>
**endFrameIndex** A zero-based index that specifies the first frame at which to stop reversing frames; the range of frames goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the value of *startFrameIndex*. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; reverses a range of frames.

#### Example

```
The following example reverses the positions of the currently selected frames:
fl.getDocumentDOM().getTimeline().reverseFrames();
The following example reverses frames from Frame 10 up to, but not including, Frame 15 (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().reverseFrames(9, 14);

```