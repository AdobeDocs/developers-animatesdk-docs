## frame.is3DMotionObject()

#### Availability

Flash Professional CS5.

#### Usage

Frame.is3DMotionObject()

#### Description

Method; a Boolean value. Lets you know whether the current selection is a 3D motion object.

#### Example

```javascript
The following example returns a trace statement informing you that the current selection is or is not a 3D motion object.
var doc = fl.getDocumentDOM();
va r my\_tl = doc.getTimeline(); this.getCurrentFr ame = func t i o n(){
var layer = my\_tl.layers\[my\_ t l. c u r re ntL aye r\]; var frame = layer .frame s\[my\_t l.curr entFrame\] ;
return frame;
}
var theFrame = getCurrentFrame(); if(theFrame.isMotionObject() && theFrame.is3DMotionObject()){ fl.trace("This selection is 3D Motion");
}else{
fl.trace("This selection is not 3D motion");
}

```