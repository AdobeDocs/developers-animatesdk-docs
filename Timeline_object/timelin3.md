## timeline.clearKeyframes()

#### Availability

> Flash MX 2004.

#### Usage

> timeline.clearKeyframes(\[startFrameIndex \[, endFrameIndex\]\])

#### Parameters

> **startFrameIndex** A zero-based index that defines the beginning of the range of frames to clear. If you omit
>
> *startFrameIndex*, the method uses the current selection. This parameter is optional.
>
> **endFrameIndex** A zero-based index that defines the end of the range of frames to clear. The range goes up to, but does not include, *endFrameIndex*. If you specify only *startFrameIndex*, *endFrameIndex* defaults to the value of *startFrameIndex*. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; converts a keyframe to a regular frame and deletes its contents on the current layer.

#### Example

> The following example clears the keyframes from Frame 5 up to, but not including, Frame 10 (remember that index values are different from frame number values):
>
> fl.getDocumentDOM().getTimeline().clearKeyframes(4, 9);
>
> The following example clears the keyframe at Frame 15 and converts it to a regular frame:
>
> fl.getDocumentDOM().getTimeline().clearKeyframes(14);
