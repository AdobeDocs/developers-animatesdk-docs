## timeline.pasteFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.pasteFrames(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

**startFrameIndex** A zero-based index that specifies the beginning of a range of frames to paste. If you omit
>
*startFrameIndex*, the method uses the current selection. This parameter is optional.
>
**endFrameIndex** A zero-based index that specifies the frame at which to stop pasting frames. The method pastes up to, but not including, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the *startFrameIndex* value. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; pastes the range of frames from the clipboard into the specified frames.

#### Example

```
The following example pastes the frames on the clipboard to the currently selected frame or playhead location:
fl.getDocumentDOM().getTimeline().pasteFrames();
The following example pastes the frames on the clipboard at Frame 2 up to, but not including, Frame 10 (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().pasteFrames(1, 9);
The following example pastes the frames on the clipboard starting at Frame 5:
fl.getDocumentDOM().getTimeline().pasteFrames(4);

```