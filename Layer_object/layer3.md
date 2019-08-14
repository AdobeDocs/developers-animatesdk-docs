## layer.frames

#### Availability

Flash MX 2004.

#### Usage

layer.frames

#### Description

Read-only property; an array of Frame objects (see [Frame object](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame_summary.md)).

#### Example

```javascript
The following example sets the variable frameArray to the array of Frame objects for the frames in the current document:
var frameArray = fl.getDocumentDOM().getTimeline().layers\[0\].frames;
To determine if a frame is a keyframe, check whether the [frame.startFrame](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame36.md) property matches the array index, as shown in the following example:
var frameArray = fl.getDocumentDOM().getTimeline().layers\[0\].frames; var n = frameArray.length;
for (i=0; i\<n; i++) {
if (i==frameArray\[i\].startFrame) { alert("Keyframe at: " + i);
}
}

```