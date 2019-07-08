## frame.motionTweenRotateTimes

#### Availability

Flash MX 2004.

#### Usage

frame.motionTweenRotateTimes

#### Description

Property; an integer that specifies the number of times the tweened element rotates between the starting keyframe and the next keyframe.

#### Example

```javascript
The following example rotates the element in this frame counter-clockwise three times by the time it reaches the next keyframe:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].motionTweenRotate = "counter- clockwise"; fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].motionTweenRotateTimes = 3;

```