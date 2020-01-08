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

Method; It will return the layer parent at the given frame.

#### Example

```javascript

var myparent = an. getDocumentDOM(). getTimeline(). layers[0]. getRigParentAtFrame (0);

```