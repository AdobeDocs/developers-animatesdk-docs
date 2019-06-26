## frame.selectMotionPath()

#### Availability

> Flash Professional CS5.

#### Usage

> Frame.selectMotionPath()

#### Description

> Method; a Boolean value. Selects (true) or deselects (false) the motion path of the current motion object.

#### Example

> The example selects or deselects the motion path of the current motion object.
>
> var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline();
>
> t his.getCurrentFrame = function(){
>
> var layer = my\_tl.layers\[my\_tl. c u rrentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
>
> }
>
> var theFrame = getCurrentFrame(); if(theFrame.isMotionObject()){
>
> if (theFrame.hasMotionPath()){ theFrame.selectMotionPath(true);
>
> }
>
> else{
>
> fl.trace("There is no motion path");
>
> }
>
> }else{
>
> fl.trace("It is no motion");
>
> }
