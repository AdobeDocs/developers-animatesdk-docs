## timeline.cutFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.cutFrames(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

**startFrameIndex** A zero-based index that specifies the beginning of a range of frames to cut. If you omit
>
*startFrameIndex*, the method uses the current selection. This parameter is optional.
>
**endFrameIndex** A zero-based index that specifies the frame at which to stop cutting. The range of frames goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the *startFrameIndex* value. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; cuts a range of frames on the current layer from the timeline and saves them to the clipboard.

#### Example

```
The following example cuts the selected frames from the timeline and saves them to the clipboard:
fl.getDocumentDOM().getTimeline().cutFrames();
The following example cuts Frame 2 up to, but not including, Frame 10 from the timeline and saves them to the clipboard (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().cutFrames(1, 9);
The following example cuts Frame 5 from the timeline and saves it to the clipboard:
fl.getDocumentDOM().getTimeline().cutFrames(4);

```