## setZoom()

#### Availability

Adobe Animate 2020

#### Usage

camera.setZoom(frameIndex, zoomVal)

#### Parameters

frameIndex:int zoomVal:int

#### Return

Nothing

#### Description

Property; Zoom camera to absolute value given by input parameter in percentage.

#### Example

The following example zooms camera to absolute value given by input parameter in percentage.
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.setZoom(37,-100);
```