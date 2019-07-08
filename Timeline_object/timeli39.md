## timeline.removeMotionObject()

#### Availability

Flash Professional CS5.

#### Usage

timeline.removeMotionObject(\[startFrame \[,endFrame\])

#### Parameters

**startFrame** Specifies the first frame at which to start removing motion objects. If you omit *startFrame*, the method uses the current selection; if there is no selection, all frames at the current playhead on all layers are removed. This parameter is optional.
**endFrame** Specifies the frame at which to stop removing motion objects; the range of frames goes up to, but does not include, *endFrame*. If you specify only *startFrame*, *endFrame* defaults to the *startFrame* value. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; removes the motion object and converts the frame(s) back to static frames. The parameters are optional, and if specified set the timeline selection to the indicated frames prior to removing the motion object.

#### Example

```javascript
The following example deletes all motion objects and converts the frames back to static frames at the current playhead position on the top layer:
fl.getDocumentDOM().getTimeline().currentLayer = 0; fl.getDocumentDOM().getTimeline().removeMotionObject();
The following example deletes motion objects from Frame 5 up to, but not including, Frame 15 of the top layer in the current scene:
fl.getDocumentDOM().getTimeline().currentLayer = 0;
fl.getDocumentDOM().getTimeline().removeMotionObject(5, 15);

```
#### See also

[timeline.createMotionObject()](#_bookmark1042)
