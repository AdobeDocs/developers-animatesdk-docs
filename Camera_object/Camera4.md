## getTint()

#### Availability

Adobe Animate 2019.

#### Usage

*camera.getTint(frameIndex)*

#### Parameters

frameIndex:int

#### Return

tint object
e.g.{percent:0,red:0,green:0,blue:0}

#### Description

Return object with two properties: ‘percent’ & ‘color’.

#### Example

The following example : 
```javascript
var timeline = an.getDocumentDOM().getTimeline();
timeline.camera.cameraEnabled = true;
timeline.camera.tintEnabled = true;
var tintVal = timeline.camera.getTint(0);
fl.trace("Tint Percentage: " + tintVal.percent +
" Red: " + tintVal.red + 
" Green: " + tintVal.green + 
" Blue: " + tintVal.blue) ;

```
#### See also

[getRotation()](../Camera_object/Camera2.md), [getZoom()](../Camera_object/Camera1.md)
