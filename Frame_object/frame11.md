## frame.hasMotionPath()

#### Availability

Flash Professional CS5.

#### Usage

*Frame.hasMotionPath()*

#### Description

Method; a Boolean value. Lets you know whether the current selection includes a motion path.

#### Example

```javascript
The following example returns a trace statement informing you if the current selection has a motion path.

var doc = fl.getDocumentDOM(); 
var my_tl = doc.getTimeline() ;
t his .getCurrentFrame = function(){
var layer =  my_tl.layers[my_tl.currentLayer]; 
var frame = layer.frames[my_tl.currentFrame]; 
return frame;
}
var theFrame = getCurrentFrame(); 
if(theFrame.isMotionObject()){
if (theFrame.hasMotionPath()){ 
    fl.trace("There is a motion path");
}else{
    fl.trace("There is no motion path");
}

```