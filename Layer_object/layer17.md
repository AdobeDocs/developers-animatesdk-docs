## layer.setColorTransformAtFrame()		

#### Availability

Animate 2020.

#### Usage

layer.setColorTransformAtFrame(frameIndex,cxformObject)		

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index.
**cxFormObject** - The cxform to be set.	

#### Returns

Nothing	

#### Description

Method; Sets the color transform at the frame.

#### Example

The following example copies the color transform of the first frame and sets it to the tenth frame:

```javascript
var myCxform = an. getDocumentDOM(). getTimeline(). layers[0].getColorTransformAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0]. setColorTransformAtFrame (9, myCxform);	
```