## frame.getMotionObjectXML()

#### Availability

Flash Professional CS5.

#### Usage

Frame.getMotionObjectXML()

#### Description

Returns a string of the motion XML from the selected motion object.

#### Example

```javascript
The following example returns the motion XML from the selected motion object.
var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline(); this.getCurrentFrame = function(){
var layer = my\_tl.layers\[my \_tl.currentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
}
var theFrame = getCurrentFrame(); if(theFrame.isMotionObject()) {
//fl.trace(theFrame.getMotionObjectXML());
}else{
fl.trace("It is not motion.");
}

```