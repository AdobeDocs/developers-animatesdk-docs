## timeline.currentFrame

#### Availability

Flash MX 2004.

#### Usage

timeline.currentFrame

#### Description

Property; the zero-based index for the frame at the current playhead location.

#### Example

```javascript
The following example sets the playhead of the current timeline to Frame 10 (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().currentFrame = 9;
The following example stores the value of the current playhead location in the curFrame variable:
var curFrame = fl.getDocumentDOM().getTimeline().currentFrame;

```