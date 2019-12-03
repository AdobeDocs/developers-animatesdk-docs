## Tween. duration

#### Availability

Flash Pro CC

#### Usage

Tween.duration

#### Description

Duration of a tween span that is equal to number of frames in a tween.

#### Example

```javascript
var tweenObj = fl.getDocumentDOM().getTimeline().layers[0].frames[0].tweenObj;
if( tweenObj.tweenType == "shape") {
for(var i = 1; i < tweenObj.duration; i++) {
var shape = tweenObj.getShape(i); ///// code to perform some operation on returned shape } }

```