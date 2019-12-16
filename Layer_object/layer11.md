## layer.getZDepthAtFrame()	

#### Availability

Adobe Animate 2020.

#### Usage

layer.getZDepthAtFrame(FrameNumber)	

#### Parameters

**FrameNumber :frame index** A string that specifies the index of the frame.	

#### Returns

ZVal:int	

#### Description

Method; An integer value that specifies the ZDepth valur at the frame.

#### Example

The following example illustrates use of this method:

```javascript
fl.getDocumentDOM().getTimeline().layers[0].getZDepthAtFrame(0)	
```