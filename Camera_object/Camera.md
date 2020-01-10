## getZDepth()

#### Availability

Adobe Animate 2019.

#### Usage

*camera.getZDepth(frameIndex)*

#### Parameters

frameIndex:int

#### Return

int


#### Description

Return current Z Depth value of camera.

#### Example

The following example :
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
var depth = timeline.camera.getZDepth(0);

```
#### See also

[getRotation()](../Camera_object/Camera2.md)
