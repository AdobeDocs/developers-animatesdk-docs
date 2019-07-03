## frame.convertMotionObjectTo2D()

#### Availability

Flash Professional CS5.

#### Usage

frame.convertMotionObjectTo2D()

#### Description

Method; Converts the selected motion object to a 2D motion object.

#### Example

```
The following example converts the selected motion object to a 2D motion object:
var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline(); this.getCurrentFrame = function(){
var layer = my\_tl.layers\[my\_tl.currentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
}
var theFrame = getCurrentFrame(); if(theFrame.isMotionObject() && the()){ theFrame.convertMotionObjectTo2D();
}else{
fl.trace("It isn't motion or it's already a 2D motion");
}

```