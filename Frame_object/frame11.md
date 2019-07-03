## frame.hasMotionPath()

#### Availability

Flash Professional CS5.

#### Usage

Frame.hasMotionPath()

#### Description

Method; a Boolean value. Lets you know whether the current selection includes a motion path.

#### Example

```
The following example returns a trace statement informing you if the current selection has a motion path.
var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline() ;
t his .getCurrentFrame = function(){
var layer = my\_tl.layers\[my\_tl.currentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
}
var theFrame = getCurrentFrame(); if(theFrame.isMotionObject()){
if (theFrame.hasMotionPath()){ fl.trace("There is a motion path");
}else{
fl.trace("There is no motion path");
}

```