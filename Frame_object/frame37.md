## frame.tweenEasing

#### Availability

Flash MX 2004.

#### Usage

*frame.tweenEasing*

#### Description

Property; an integer that specifies the amount of easing that should be applied to the tweened object. Acceptable values are -100 to 100. To begin the motion tween slowly and accelerate the tween toward the end of the animation, use a value between -1 and -100. To begin the motion tween rapidly and decelerate the tween toward the end of the animation, use a positive value between 1 and 100.

#### Example

```javascript
The following example specifies that the motion of the tweened object should begin fairly rapidly and decelerate toward the end of the animation:

fl.getDocumentDOM().getTimeline().layers[0].frames[0].tweenEasing = 50;

```