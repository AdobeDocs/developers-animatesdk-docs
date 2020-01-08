## setTint()

#### Availability

Adobe Animate 2019.

#### Usage

camera.setRotation(frameIndex, amount, red, green, blue)

#### Parameters

frameIndex:int amount:int red:int green:int blue:int

#### Return

nothing

#### Description

Property; Set camera tint using tint color(RGB) & tint percent (percentage of tint).

#### Example

The following example sets camera tint using tint color(RGB) & tint percent (percentage of tint).
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
timeline.camera.tintEnabled = true;

timeline.camera.setTint(0, 100,255,255,255 );

```