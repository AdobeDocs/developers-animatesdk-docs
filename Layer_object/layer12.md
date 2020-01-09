## layer.setZDepthAtFrame()	

#### Availability

Animate 2019.

#### Usage

layer.setZDepthAtFrame(FrameNumber,ZVal)	

#### Parameters

**FrameNumber** : It is an integer that specifies the frame index starting from 0. 
**ZVal**: It is an integer that specifies the ZDepth value ranges between -5000 to 10000.

#### Returns

Nothing	

#### Description

Method; Sets the ZDepth at the specified frame number.

#### Example

The following example sets the zdepth value at first frame to 100 of the first layer: 

```javascript
fl.getDocumentDOM().getTimeline().layers[0].setZDepthAtFrame(0,100);
```