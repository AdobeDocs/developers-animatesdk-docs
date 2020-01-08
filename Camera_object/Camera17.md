## camera.cameraEnabled	

#### Availability

Animate 2019

#### Usage

camera.cameraEnabled	

#### Return

Boolean value true if camera is enabled otherwise false.

#### Description

Property; Used to Enable/Disable camera.

#### Example

The following example enables the camera:

```javascript
var timeline = an.getDocumentDOM().getTimeline();

fl.trace(timeline.camera.cameraEnabled = true);
```