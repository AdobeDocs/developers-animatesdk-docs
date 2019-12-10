## layer.setColorTransformAtFrame()		

#### Availability

Adobe Animate 2020.

#### Usage

layer.setColorTransformAtFrame(frameIndex,cxformObject)		

#### Parameters

frameIndex – int, cxFormObject - The cxform to be set	

#### Returns

none	

#### Description

Method; 

#### Example

The following example illustrates use of this method:


```javascript
var myCxform = an. getDocumentDOM(). getTimeline(). layers[0].getColorTransformAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0]. setColorTransformAtFrame (9, myCxform);	
```