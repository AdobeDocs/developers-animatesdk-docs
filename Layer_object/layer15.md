## layer.getFiltersAtFrame()	

#### Availability

Animate 2020.

#### Usage

layer.getFiltersAtFrame(frameIndex)		

#### Parameters

**frameIndex** - It is an integer that specifies absolute frame index.

#### Returns

An array that contains a list of filters applied to the frame at frameIndex

#### Description

Method; An array that contains a list of filters applied to the frame at frameIndex. 

#### Example

The following example gets the filters at the first frame of the first layer:

```javascript
var myFilters = an.getDocumentDOM().getTimeline().layers[0].getFiltersAtFrame(0);	
```