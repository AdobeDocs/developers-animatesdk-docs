## timeline.createMotionTween()

#### Availability

> Flash MX 2004.

#### Usage

> timeline.createMotionTween(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

> **startFrameIndex** A zero-based index that specifies the beginning frame at which to create a motion tween. If you omit *startFrameIndex*, the method uses the current selection. This parameter is optional.
>
> **endFrameIndex** A zero-based index that specifies the frame at which to stop the motion tween. The range of frames goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the *startFrameIndex* value. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; sets the [frame.tweenType](#_bookmark641) property to motion for each selected keyframe on the current layer, and converts each frame’s contents to a single symbol instance if necessary. This property is the equivalent to the Create Motion Tween menu item in the Flash authoring tool.

#### Example

> The following example converts the shape in the first frame up to, but not including, Frame 10 to a graphic symbol instance and sets the frame.tweenType to motion (remember that index values are different from frame number values):
>
> fl.getDocumentDOM().getTimeline().createMotionTween(0, 9);
