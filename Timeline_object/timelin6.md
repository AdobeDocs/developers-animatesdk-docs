## timeline.copyFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.copyFrames([startFrameIndex [, endFrameIndex]])

#### Parameters

**startFrameIndex** A zero-based index that specifies the beginning of the range of frames to copy. If you omit
*startFrameIndex*, the method uses the current selection. This parameter is optional.
**endFrameIndex** A zero-based index that specifies the frame at which to stop copying. The range of frames to copy goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the value of *startFrameIndex*. This parameter is optional.

#### Returns

Nothing.s

#### Description

Method; copies a range of frames on the current layer to the clipboard.

#### Example


The following example copies the selected frames to the clipboard:
```javascript
fl.getDocumentDOM().getTimeline().copyFrames();
```
The following example copies Frame 2 up to, but not including, Frame 10, to the clipboard (remember that index values are different from frame number values):
```javascript
fl.getDocumentDOM().getTimeline().copyFrames(1, 9);
```
The following example copies Frame 5 to the clipboard:
```javascript
fl.getDocumentDOM().getTimeline().copyFrames(4);
```