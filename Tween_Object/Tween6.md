## Tween. tweenType

#### Availability

Flash Pro CC

#### Usage

Tween.tweenType

#### Description

Specifies the type of tween. For example, Motion or Shape.

#### Example

```
var tweenObj = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].tweenObj; if( tweenObj.tweenType == "shape") {
for(var i = 1; i \< tweenObj.duration; i++) {
var shape = tweenObj.getShape(i); ///// code to perform some operation on returned shape } }

```