## frame.isMotionObject()

#### Availability

Flash Professional CS5.

#### Usage

*Frame.isMotionObject()*

#### Description

Method; a Boolean value. Lets you know whether the current selection is a motion object.

#### Example

```javascript
The following example returns a trace statement informing you that the current selection is or is not a motion object.

var my_tl = doc.getTimeline() ; 
this.getCurrentFrame = function(){
var layer = my_tl.layers[my_tl.currentLayer];
var frame = layer.frames[my_tl.currentFrame]; 
return frame;
}
var theFrame = getCurrentFrame(); 
if(theFrame.isMotionObject()) { 
    fl.trace("This selection is motion.");
}else{
    fl.trace("This selection is not motion.");
}

```