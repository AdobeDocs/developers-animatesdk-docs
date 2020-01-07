## layer.getColorTransformAtFrame()	

#### Availability

Animate 2020.

#### Usage

layer.getColorTransformAtFrame(frameIndex)		

#### Parameters

**frameIndex** - int (absolute frame index)

#### Returns

Value object 

#### Description

Returns: Value object {“mode”,”tintPercent”,”tintRed”,”tintBlue”,”tintGreen”,”brightnessPercent”,”alphaPercent”,"colorAlphaAmount", "colorAlphaPercent", "colorRedAmount", "colorRedPercent", "colorGreenAmount", "colorGreenPercent", "colorBlueAmount", "colorBluePercent"}.

Based on the mode, the paramters will be updated here. For example, if tint is present, the value corresponding to tint only will be present along with the color matrix values.

#### Example

The following example illustrates use of this method:


```javascript
var myCxform = an.getDocumentDOM().getTimeline().layers[0]. getColorTransformAtFrame (0);
```