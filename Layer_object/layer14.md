## layer.getColorTransformAtFrame()	

#### Availability

Animate 2020.

#### Usage

layer.getColorTransformAtFrame(frameIndex)		

#### Parameters

**frameIndex** - It is an integer that specifies absolute frame index.

#### Returns

Value object 

#### Description

Returns: Value object {“mode”,”tintPercent”,”tintRed”,”tintBlue”,”tintGreen”,”brightnessPercent”,”alphaPercent”,"colorAlphaAmount", "colorAlphaPercent", "colorRedAmount", "colorRedPercent", "colorGreenAmount", "colorGreenPercent", "colorBlueAmount", "colorBluePercent"}.

Based on the mode, the paramters will be updated here. For example, if tint is present, the value corresponding to tint only will be present along with the color matrix values.

#### Example

The following example gets the color transform of the fifth frame of first layer:

```javascript
var myCxform = an.getDocumentDOM().getTimeline().layers[0]. getColorTransformAtFrame (4);
```