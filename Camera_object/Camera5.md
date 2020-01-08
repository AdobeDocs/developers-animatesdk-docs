## getColorFilter()

#### Availability

Adobe Animate 2019.

#### Usage

camera.getColorFilter(frameIndex)

#### Parameters

frameIndex:int

#### Return

object
e.g.{brightness:0,contrast:0,saturation:0,hue:0}

#### Description

Property; Get camera color filter.

#### Example

The following example gets camera color filter.
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
timeline.camera.colorFilterEnabled = true;
var filterVal = timeline.camera.getColorFilter(0);
fl.trace(" Brightness: " + filterVal.brightness +
" Contrast: " + filterVal.contrast+ 
" Saturation: " + filterVal.saturation + 
" Hue: " + filterVal.hue);

```