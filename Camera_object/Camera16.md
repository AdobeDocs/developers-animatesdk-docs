## reset()

#### Availability

Adobe Animate 2019.

#### Usage

camera.reset(frameIndex)

#### Parameters

frameIndex:int

#### Return

Nothing

#### Description

Reset all camera properties to default.

#### Example

The following example reset all camera properties to default.
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.reset(0);
```
