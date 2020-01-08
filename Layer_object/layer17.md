## layer.setColorTransformAtFrame()		

#### Availability

Animate 2020.

#### Usage

layer.setColorTransformAtFrame(frameIndex,cxformObject)		

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index.
**cxFormObject** - The cxform to be set	

#### Returns

none	

#### Description

Method; Sets the color transform at a particular frame.

#### Example

The following example illustrates use of this method:


```javascript
var myCxform = an. getDocumentDOM(). getTimeline(). layers[0].getColorTransformAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0]. setColorTransformAtFrame (9, myCxform);	
```