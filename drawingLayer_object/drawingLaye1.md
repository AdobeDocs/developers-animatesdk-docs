## drawingLayer.beginFrame()

#### Availability

Flash MX 2004.

#### Usage

*drawingLayer.beginFrame()*

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; erases what was previously drawn using the drawingLayer and prepares for more drawing commands. Should be called after drawingLayer.beginDraw(). Everything drawn between *drawingLayer.beginFrame()* and an *drawingLayer.endFrame()* remains on the Stage until you call the next *beginFrame()* and *endFrame()*. (In this context, *frame* refers to where you start and end drawing; it does not refer to timeline frames.) You typically use this method only when creating extensible tools. See [drawingLayer.beginDraw()](../drawingLayer_object/drawingLayer.md).
