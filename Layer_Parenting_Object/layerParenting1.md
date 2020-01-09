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

The following example gets the layer parent of the first frame of the layer index 0:

```javascript

var myparent = an. getDocumentDOM(). getTimeline(). layers[0]. getRigParentAtFrame (0);

```