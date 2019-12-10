## layer.setBlendModeAtFrame()	

#### Availability

Adobe Animate 2020.

#### Usage

layer.setBlendModeAtFrame(frameIndex,blendModeString)		

#### Parameters

frameIndex – int , blendModeString - The blendmode to be set	

#### Returns

none		

#### Description

Method; 

#### Example

The following example illustrates use of this method:


```javascript
var myBlend = an. getDocumentDOM(). getTimeline(). layers[0].getBlendModeAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0]. setBlendModeAtFrame (9, myBlend);	
```