## Tween object Summary

#### Availability

Flash Pro CC.

#### Description

The Tween object can be used to access interpolated properties of tweens. Accessing properties for a non-tween frame throws errors.

#### Method Summary

You can use the following methods with the Tween object class:

<table><thead><tr class="header"><th><strong>Method</strong></th><th><p><strong>Description</strong></p></th></tr></thead><tbody><tr class="odd"><td><a href="../Tween_Object/Tween.md">"Tween.getCol orTransform( )"</a> on page 571 </td><td><p>Returns color transformation data between frames.</p></td></tr><tr class="even"><td><p><a href="../Tween_Object/Tween1.md">"Tween.getFilters( )"</a> on page 572 </td><td><p>Returns filters data of a selected frame from a tween span.</p></td></tr><tr class="odd"><td><a href="../Tween_Object/Tween2.md">"Tween. getGeometricT ransform()"</a> on page 572 </td><td><p>Returns Matrix object that represents geometric transformation of a tween within a user-defined range (from offset to a selected frame).</p></td></tr><tr class="even"><td><a href="../Tween_Object/Tween3.md">"Tween. getShape( )"</a> on page 573 </td><td><p>Returns interpolated shape of a selected frame within a tween-span.</p></td></tr></tbody></table>

#### Properties Summary

You can use the following properties within methods of Tween object class:

<table><thead><tr class="header"><th><strong>Property</strong></th><th><p><strong>Description</strong></p></th></tr></thead><tbody><tr class="odd"><td><a href="../Tween_Object/Tween4.md">"Tween. duration" </a>on page 573</td><td><p>Duration of a tween span that is equal to number of frames in a tween.</p></td></tr><tr class="even"><td><a href="../Tween_Object/Tween5.md">"Tween. startFrame" </a>on page 574</td><td><p>Start frame of a tween.</p></td></tr><tr class="odd"><td><a href="../Tween_Object/Tween6.md">"Tween. tweenType" </a>on page 574</td><td><p>Specifies the type of tween. For example, Motion or Shape.</p></td></tr></tbody></table>

#### Usage

var mat;
var frame = fl.getDocumentDOM().getTimeline().layers[0].frames[0];
var tweenObj = frame.tweenObj;
var frame1 = fl.getDocumentDOM().getTimeline().layers[1].frames[0];
fl.trace(" Tween duration = " + tweenObj.duration);
for(var i = 1; i < tweenObj.duration; i++) {
mat = tweenObj.getGeometricTransform(i);
var colors = tweenObj.getColorTransform(i);
fl.trace(" Frame " + i + " Matrix = a = " + mat.a + " b = " + mat.b + " c = " + mat.c + " d =
" + mat.d + " tx = " + mat.tx + " ty = " + mat.ty );
fl.trace(" color transform :");
fl.trace(" alpha : amount = "+colors.colorAlphaAmount+" percent = "+colors.colorAlphaPercent);
fl.trace(" red : amount = "+colors.colorRedAmount+" percent = "+colors.colorRedPercent);
fl.trace(" green : amount = "+colors.colorGreenAmount+" percent = "+colors.colorGreenPercent);
fl.trace(" blue : amount = "+colors.colorBlueAmount+" percent = "+colors.colorBluePercent); }

<span id="Tween.getColorTransform(_)" class="anchor"></span>

