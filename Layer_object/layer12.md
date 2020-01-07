## layer.setZDepthAtFrame()	

#### Availability

Adobe Animate 2019.

#### Usage

layer.setZDepthAtFrame(FrameNumber,ZVal)	

#### Parameters

**FrameNumber** :frame index, 
**ZVal**:int

#### Returns

nothing	

#### Description

Sets the ZDepth value at the specified frame number.

#### Example

The following example illustrates use of this method:


```javascript
fl.getDocumentDOM().getTimeline().layers[0].setZDepthAtFrame(0,900)	
```