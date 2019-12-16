## layer.setRigParentAtFrame()

#### Availability

Adobe Animate 2020.

#### Parameters

**frameIndex** – int
**layer** - The layer object to be set as parent

#### Usage

 layer.setRigParentAtFrame(frameIndex,layer) 
 
#### Returns

none

#### Example

```javascript

var myParent=an.getDocumentDOM().

getTimeline().layers[0].getRigParentAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0].setRigParentAtFrame (9, myParent);


```