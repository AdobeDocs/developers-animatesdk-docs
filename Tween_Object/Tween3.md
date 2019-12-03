## Tween. getShape( )

#### Availability

Flash Pro CC.

#### Usage

Tween.getShape( )

#### Parameters

**FrameIndex** Offset index of the frame from which shape data has to be retrieved.

#### Returns

Returns shape coordinates at the frame offset.

#### Description

Method; Returns interpolated shape of a selected frame within a tween-span.

#### Usage

var tweenObj = fl.getDocumentDOM().getTimeline().layers[0].frames[0].tweenObj;if( tweenObj.tweenType ==
"shape") {for(var i = 1; i < tweenObj.duration; i++) {var shape = tweenObj.getShape(i); ///// code to perform some
operation on returned shape } }

