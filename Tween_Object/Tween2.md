## Tween. getGeometricTransform()

#### Availability

Flash Pro CC.

#### Usage

Tween. getGeometricTransform(frameIndex)

#### Parameters

**FrameIndex** Offset index of the frame from which geometric transformations have to be retrieved.

#### Returns

Matrix object that represents geometric transformations at the frame offset.

#### Description

Method; Returns Matrix object that represents geometric transformation of a tween within a user-defined range (from offset to a selected frame).

#### Usage

var mat;
var frame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\]; var tweenObj = frame.tweenObj;
var frame1 = fl.getDocumentDOM().getTimeline().layers\[1\].frames\[0\]; fl.trace(" Tween duration = " + tweenObj.duration);
for(var i = 1; i \< tweenObj.duration; i++) { mat = tweenObj.getGeometricTransform(i);
var colors = tweenObj.getColorTransform(i);
fl.trace(" Frame " + i + " Matrix = a = " + mat.a + " b = " + mat.b + " c = " + mat.c + " d = " + mat.d + " tx = " + mat.tx + " ty = " + mat.ty );
fl.trace(" color transform :");
fl.trace(" alpha : amount = "+colors.colorAlphaAmount+" percent = "+colors.colorAlphaPercent); fl.trace(" red : amount = "+colors.colorRedAmount+" percent = "+colors.colorRedPercent); fl.trace(" green : amount = "+colors.colorGreenAmount+" percent = "+colors.colorGreenPercent); fl.trace(" blue : amount = "+colors.colorBlueAmount+" percent = "+colors.colorBluePercent); }

