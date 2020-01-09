## layer.getRigParentAtFrame()

#### Availability

Adobe Animate 2020.

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index.

#### Usage

layer.getRigParentAtFrame(frameIndex) 

#### Returns

layer object

#### Description

Method; It will return the layer parent of the given frame.

#### Example

The following example gets the layer parent from the first frame of the ninth layer:

```javascript

var myparent = an. getDocumentDOM(). getTimeline(). layers[8]. getRigParentAtFrame (0);

```