## layer.getZDepthAtFrame()	

#### Availability

Adobe Animate 2019.

#### Usage

layer.getZDepthAtFrame(FrameNumber)	

#### Parameters

**FrameNumber :frame index** An integer specifying the frame index	number starting from 0.

#### Returns

ZVal:int	

#### Description

An integer value that specifies the ZDepth value of the frame.

#### Example

The following example illustrates use of this method:

```javascript
fl.getDocumentDOM().getTimeline().layers[0].getZDepthAtFrame(0)	
```