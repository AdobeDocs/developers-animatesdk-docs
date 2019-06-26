## frame.setMotionObjectXML()

#### Availability

> Flash Professional CS5.

#### Usage

> frame.setMotionObjectXML( xmlstr \[, endAtCurrentLocation\] )

#### Parameters

> **xmlstr** A string value that specifies the XML string.
>
> **endAtCurrentLocation** A boolean value that determines whether the tween starts or ends at the current position.

#### Description

> Method; applies the specified motion XML to the selected motion object.

#### Example

> This example specifies that the motion XML identified as myMotionXML be applied to the selected motion object.
>
> var doc = fl.getDocumentDOM(); var my\_tl = doc.getTimeline();
>
> this.getCurrentFrame = function(){
>
> var layer = my\_tl.layers\[my\_tl.currentLayer\]; var frame = layer.frames\[my\_tl.currentFrame\]; return frame;
>
> }
>
> var theFrame = getCurrentFrame(); theFrame.setMotionObjectXML(myMotionXML.toString(), false);
