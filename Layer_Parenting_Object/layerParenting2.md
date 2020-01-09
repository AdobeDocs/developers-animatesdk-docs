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

#### Description

Method; It will set the layer parent at the particular frame.

#### Example

In the following example it copies the layer parent applied at the first frame and sets it to the tenth frame of the first layer:

```javascript

var myParent=an.getDocumentDOM().

getTimeline().layers[0].getRigParentAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0].setRigParentAtFrame (9, myParent);


```