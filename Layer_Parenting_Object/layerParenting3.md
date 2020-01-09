## layer.getRigMatrixAtFrame()

#### Availability

Adobe Animate 2020.

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index.

#### Usage

layer.getRigMatrixAtFrame(frameIndex)

#### Returns

matrix object

#### Description

Method; It will return the rig matrix of the particular frame.

#### Example

The following example gets the rig matrix from the first frame of the ninth layer:

```javascript

var matrix = an. getDocumentDOM(). getTimeline(). layers[8]. getRigMatrixAtFrame (0);

```
