## layer.getBlendModeAtFrame()	

#### Availability

Adobe Animate 2020.

#### Usage

layer.getBlendModeAtFrame(frameIndex)		

#### Parameters

frameIndex - int (absolute frame index)	

#### Returns

blendmode string

#### Description

Method; 

#### Example

The following example illustrates use of this method:


```javascript
var myblend= an.getDocumentDOM().getTimeline().layers[0]. getBlendModeAtFrame (0);
```