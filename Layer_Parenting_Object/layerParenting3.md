## layer.getRigMatrixAtFrame()

#### Availability

Adobe Animate 2020.

#### Parameters

**frameIndex** – int

#### Usage

layer.getRigMatrixAtFrame(frameIndex)

#### Returns

matrix object

#### Description

Method; It will return the rig matrix at the particular frame.

#### Example

The following example gets the rig matrix of the first frame of the first layer:

```javascript

var matrix = an. getDocumentDOM(). getTimeline(). layers[0]. getRigMatrixAtFrame (0);

```
