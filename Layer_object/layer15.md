## layer.getFiltersAtFrame()	

#### Availability

Adobe Animate 2020.

#### Usage

layer.getFiltersAtFrame(frameIndex)		

#### Parameters

frameIndex - int (absolute frame index)	

#### Returns

An array that contains a list of filters applied to the frame at frameIndex

#### Description

Method; 

#### Example

The following example illustrates use of this method:


```javascript
var myFilters = an.getDocumentDOM().getTimeline().layers[0].getFiltersAtFrame(0);	
```