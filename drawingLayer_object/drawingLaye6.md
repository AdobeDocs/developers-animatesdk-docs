## drawingLayer.endFrame()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.endFrame()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; signals the end of a group of drawing commands. A group of drawing commands refers to everything drawn between [drawingLayer.beginFrame()](#_bookmark348) and drawingLayer.endFrame(). The next call to [drawingLayer.beginFrame()](#_bookmark348) will erase whatever was drawn in this group of drawing commands. You typically use this method only when creating extensible tools.
