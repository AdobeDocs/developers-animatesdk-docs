## frame.convertMotionObjectTo3D()

#### Availability

Flash Professional CS5.

#### Usage

*frame.convertMotionObjectTo3D()*

#### Description

Method; Converts the selected motion object to a 3D motion object.

#### Example

```javascript
The following example converts the selected motion object to a 3D motion object:

var doc = fl.getDocumentDOM();
v a r my_tl = doc.getTimeline(); 
this.getCurrentF r ame = functi on() {
var layer = my_tl.layers[my  _tl.cu  rrentLa yer]; 
var frame = layer.frames[my_tl.currentFrame ]; 
retur n frame;
}
var theFrame = getCurrentFrame();
if(theFrame.isMotionObject() && !theFrame.is3DMotionObject()){ theFrame.convertMotionObjectTo3D();
}else{
fl.trace("It isn't motion or it's already a 3D motion");
}

```