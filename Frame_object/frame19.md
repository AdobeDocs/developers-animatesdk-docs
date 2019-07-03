## frame.motionTweenScale

#### Availability

Flash MX 2004.

#### Usage

frame.motionTweenScale

#### Description

Property; a Boolean value that specifies whether the tweened element scales to the size of the object in the following keyframe, increasing its size with each frame in the tween (true), or doesn’t scale (false).

#### Example

```
The following example specifies that the tweened element should scale to the size of the object in the following keyframe, increasing its size with each frame in the tween.
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].motionTweenScale = true;

```