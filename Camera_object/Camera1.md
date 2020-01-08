## getZoom()

#### Availability

Adobe Animate 2019.

#### Usage

*camera.getZoom(frameIndex)*

#### Parameters

frameIndex:int

#### Return

double

#### Description

Property; Return the current zoom value of camera. Default is 100%.

#### Example

The following example :

```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
var zoomval = timeline.camera.getZoom(0);

```
#### See also

[getZDepth()](../Camera_object/Camera.md), [getRotation()](../Camera_object/Camera2.md)
