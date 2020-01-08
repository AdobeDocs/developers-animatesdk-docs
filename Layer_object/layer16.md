## layer.setBlendModeAtFrame()

#### Availability

Animate 2020.

#### Usage

layer.setBlendModeAtFrame(frameIndex,blendModeString)	

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index. 
**blendModeString** - It is the string that specifies the blendmode to be set.

#### Returns

none

#### Description

Method; Sets the blending mode at the particular frame.

#### Example

The following example sets the blending mode at the frame index 9.


```javascript
var myBlend = an. getDocumentDOM(). getTimeline(). layers[0].getBlendModeAtFrame (0);

an.getDocumentDOM().getTimeline().layers[0]. setBlendModeAtFrame (9, myBlend);
```