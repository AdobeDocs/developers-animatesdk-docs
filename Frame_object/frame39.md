## frame.tweenType

#### Availability

Flash MX 2004.

#### Usage

frame.tweenType

#### Description

Property; a string that specifies the type of tween; acceptable values are "motion", "shape", or "none". The value
"none" removes the motion tween. Use the [timeline.createMotionTween()](#_bookmark1044) method to create a motion tween.
If you specify "motion", the object in the frame must be a symbol, text field, or grouped object. It will be tweened from its location in the current keyframe to the location in the following keyframe.
If you specify "shape", the object in the frame must be a shape. It will blend from its shape in the current keyframe to the shape in the following keyframe.

#### Example

```
The following example specifies that the object is a motion tween, and therefore, it should be tweened from its location in the current keyframe to the location in the following keyframe:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].tweenType = "motion";

```