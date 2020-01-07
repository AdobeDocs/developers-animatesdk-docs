## layer.getBlendModeAtFrame()	

#### Availability

Animate 2020.

#### Usage

layer.getBlendModeAtFrame(frameIndex)		

#### Parameters

**frameIndex** - int (absolute frame index)	

#### Returns

blendmode string

#### Description

Method; A string value that specifies the blend mode at frame.

#### Example

The following example illustrates use of this method:


```javascript
var myblend= an.getDocumentDOM().getTimeline().layers[0]. getBlendModeAtFrame (0);
```