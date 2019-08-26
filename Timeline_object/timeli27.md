## timeline.insertBlankKeyframe()

#### Availability

Flash MX 2004.

#### Usage

timeline.insertBlankKeyframe(\[frameNumIndex\])

#### Parameters

**frameNumIndex** A zero-based index that specifies the frame at which to insert the keyframe. If you omit
*frameNumIndex*, the method uses the current playhead frame number. This parameter is optional.
If the specified or selected frame is a regular frame, the keyframe is inserted at the frame. For example, if you have a span of 10 frames numbered 1-10 and you select Frame 5, this method makes Frame 5 a blank keyframe, and the length of the frame span is still 10 frames. If Frame 5 is selected and is a keyframe with a regular frame next to it, this method inserts a blank keyframe at Frame 6. If Frame 5 is a keyframe and the frame next to it is already a keyframe, no keyframe is inserted but the playhead moves to Frame 6.

#### Returns

Nothing.

#### Description

Method; inserts a blank keyframe at the specified frame index; if the index is not specified, the method inserts the blank keyframe by using the playhead/selection. See also [timeline.insertKeyframe()](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeli29.md).

#### Example

```javascript
The following example inserts a blank keyframe at Frame 20 (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().insertBlankKeyframe(19);
The following example inserts a blank keyframe at the currently selected frame (or playhead location if no frame is selected):
fl.getDocumentDOM().getTimeline().insertBlankKeyframe();

```