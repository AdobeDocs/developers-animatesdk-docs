## setRotation()

#### Availability

Adobe Animate 2020

#### Usage

camera.setRotation(frameIndex, rotation)

#### Parameters

frameIndex:int rotation:int

#### Return

nothing

#### Description

Property; Rotate camera by absolute angle given as input parameters.

#### Example

The following example rotates camera by absolute angle given as input parameters.
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.setRotation(37,-100);
```