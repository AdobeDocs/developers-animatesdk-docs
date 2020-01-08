## setColorFilter()

#### Availability

Adobe Animate 2019.

#### Usage

camera.setColorFilter(frameIndex, brightness, contrast, saturation, hue)

#### Parameters

frameIndex:int brightness:number contrast:number saturation:number hue:number

#### Return

nothing

#### Description

Property; Set camera color filter using decomposed values of (Brightness,Contrast,saturation,hue).

#### Example

The following example sets Set camera color filter using decomposed values of (Brightness,Contrast,saturation,hue).
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
timeline.camera.colorFilterEnabled = true;

timeline.camera.setColorFilter(0, 50, 255, 255, 100);

```