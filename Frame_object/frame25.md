## frame.setMotionObjectDuration()

#### Availability

Flash Professional CS5.

#### Usage

Frame.setMotionObjectDuration( duration \[, stretchExistingKeyframes\] )

#### Parameters

**duration** Specifies the number of frames for the tween span of the selected motion object.
**stretchExistingKeyframes** A boolean value that determines whether the tween span is stretched, or if frames are added, to the end of the last frame.

#### Description

Method; sets the duration (the tween span length) of the currently selected motion object.

#### Example

```
The following example specifies a duration of 11 frames for the selected motion object.
var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline();
this.getCurrentFrame = function(){
var layer = my\_tl.layers\[my\_tl.currentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
}
var theFrame = getCurrentFrame(); if(theFrame.isMotionObject()){ theFrame.setMotionObjectDuration(11);
}else{
fl.trace("It isn't motion");
}

```