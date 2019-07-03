## timeline.insertKeyframe()

#### Availability

Flash MX 2004.

#### Usage

timeline.insertKeyframe(\[frameNumIndex\])

#### Parameters

**frameNumIndex** A zero-based index that specifies the frame index at which to insert the keyframe in the current layer. If you omit *frameNumIndex*, the method uses the frame number of the current playhead or selected frame. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; inserts a keyframe at the specified frame. If you omit the parameter, the method inserts a keyframe using the playhead or selection location.
>
This method works the same as [timeline.insertBlankKeyframe()](#_bookmark1061) except that the inserted keyframe contains the contents of the frame it converted (that is, it’s not blank).

#### Example

```
The following example inserts a keyframe at the playhead or selected location:
fl.getDocumentDOM().getTimeline().insertKeyframe();
The following example inserts a keyframe at Frame 10 of the second layer (remember that index values are different from frame or layer number values):
fl.getDocumentDOM().getTimeline().currentLayer = 1; fl.getDocumentDOM().getTimeline().insertKeyframe(9);

```