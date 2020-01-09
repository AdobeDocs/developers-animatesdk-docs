## setRotation()

#### Availability

Adobe Animate 2019

#### Usage

camera.setRotation(frameIndex, angleDegree)

#### Parameters

frameIndex:int - frame Number in timeline

AngleDegree:int - the angleDegree for rotation.

#### Return

nothing

#### Description

Rotate camera by absolute angle given as input parameters.

#### Example

The following example rotates camera by absolute angle given as input parameters.
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.setRotation(37,-100);
```