## getRotation()

#### Availability

Adobe Animate 2019.

#### Usage

*camera.getRotation(frameIndex)*

#### Parameters

frameIndex:int

#### Return

int

#### Description

Property; Return current angle of camera.

#### Example

The following example :

```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
var val = timeline.camera.getRotation(0);
```


#### See also

[getZDepth()](../Camera_object/Camera.md), [getRotation()](../Camera_object/Camera2.md), [getZoom()](../Camera_object/Camera1.md)