## Tween.getFilters( )

#### Availability

Flash Pro CC.

#### Usage

Tween.getFilters(frameIndex);

#### Parameters

**FrameIndex** Index of the frame from which filter data is to be retrieved.

#### Returns

Returns array of Filter objects.

#### Description

Method; Returns filters data of a selected frame from a tween span.

#### Usage

var tweenObj = fl.getDocumentDOM().getTimeline().layers[0].frames[0].tweenObj;\
 for( var i = 0; i < tweenObj.duration; i++) { \
var filterList = tweenObj.getFilters(i);\
 for( var j = 0; j< filterList.length; j++) { \
 var filter = filterList[j];\
  fl.trace(filter.name);\
fl.trace("Blur x = " + filter.blurX + " y = " + filter.blurY); } }

