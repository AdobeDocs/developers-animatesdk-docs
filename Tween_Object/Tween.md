## Tween.getColorTransform( )

#### Availability

Flash Pro CC.

#### Usage

Tween.getGeometricTransform(frameIndex)

#### Parameters

**frameIndex** Offset index of interpolated frame.

#### Returns

Value object {"colorAlphaAmount", "colorAlphaPercent", "colorRedAmount", "colorRedPercent", "colorGreenAmount", "colorGreenPercent", "colorBlueAmount", "colorBluePercent"}.

#### Description

Method; Gets color transformation data between frames.

#### Usage

var mat;\
var frame = fl.getDocumentDOM().getTimeline().layers[0].frames[0];\
var tweenObj = frame.tweenObj;\
var frame1 = fl.getDocumentDOM().getTimeline().layers[1].frames[0];\
 fl.trace(" Tween duration = " + tweenObj.duration);\
for(var i = 1; i < tweenObj.duration; i++)
 { \
     mat = tweenObj.getGeometricTransform(i);\
var colors = tweenObj.getColorTransform(i);\
fl.trace(" Frame " + i + " Matrix = a = " + mat.a + " b = " + mat.b + " c = " + mat.c + " d = " + mat.d + " tx = " + mat.tx + " ty = " + mat.ty );\
fl.trace(" color transform :");

