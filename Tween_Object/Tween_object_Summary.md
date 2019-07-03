## Tween object Summary

#### Availability

Flash Pro CC.

#### Description

The Tween object can be used to access interpolated properties of tweens. Accessing properties for a non-tween frame throws errors.

#### Method Summary

You can use the following methods with the Tween object class:

<table><thead><tr class="header"><th><strong>Method</strong></th><th><p><strong>Description</strong></p></th></tr></thead><tbody><tr class="odd"><td><a href="#Tween.getColorTransform(_)">"Tween.getCol orTransform( )"</a<a href="#Tween.getColorTransform(_)">on page 571</a></td><td><p>Returns color transformation data between frames.</p></td></tr><tr class="even"><td><p><a href="#_bookmark1126">"Tween.getFilte rs( )" on</a></p><p><a href="#_bookmark1126">page 572</a></p></td><td><p>Returns filters data of a selected frame from a tween span.</p></td></tr><tr class="odd"><td><a href="#_bookmark1127">"Tween. getGeometricT ransform()" on</a<a href="#_bookmark1127">page 572</a></td><td><p>Returns Matrix object that represents geometric transformation of a tween within a user-defined range (from offset to a selected frame).</p></td></tr><tr class="even"><td><a href="#_bookmark1128">"Tween. getShape( )" on</a<a href="#_bookmark1128">page 573</a></td><td><p>Returns interpolated shape of a selected frame within a tween-span.</p></td></tr></tbody></table>

#### Properties Summary

You can use the following properties within methods of Tween object class:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><p><strong>Description</strong></p></th></tr></thead><tbody><tr class="odd"><td><a href="#_bookmark1129">"Tween. duration" on</a<a href="#_bookmark1129">page 573</a></td><td><p>Duration of a tween span that is equal to number of frames in a tween.</p></td></tr><tr class="even"><td><a href="#_bookmark1130">"Tween. startFrame" on</a<a href="#_bookmark1130">page 574</a></td><td><p>Start frame of a tween.</p></td></tr><tr class="odd"><td><a href="#_bookmark1131">"Tween. tweenType" on</a<a href="#_bookmark1131">page 574</a></td><td><p>Specifies the type of tween. For example, Motion or Shape.</p></td></tr></tbody></table>

#### Usage

var mat;
var frame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\]; var tweenObj = frame.tweenObj;
var frame1 = fl.getDocumentDOM().getTimeline().layers\[1\].frames\[0\]; fl.trace(" Tween duration = " + tweenObj.duration);
for(var i = 1; i \< tweenObj.duration; i++) { mat = tweenObj.getGeometricTransform(i);
var colors = tweenObj.getColorTransform(i);
fl.trace(" Frame " + i + " Matrix = a = " + mat.a + " b = " + mat.b + " c = " + mat.c + " d = " + mat.d + " tx = " + mat.tx + " ty = " + mat.ty );
fl.trace(" color transform :");
fl.trace(" alpha : amount = "+colors.colorAlphaAmount+" percent = "+colors.colorAlphaPercent); fl.trace(" red : amount = "+colors.colorRedAmount+" percent = "+colors.colorRedPercent); fl.trace(" green : amount = "+colors.colorGreenAmount+" percent = "+colors.colorGreenPercent); fl.trace(" blue : amount = "+colors.colorBlueAmount+" percent = "+colors.colorBluePercent); }

<span id="Tween.getColorTransform(_)" class="anchor"></span>

