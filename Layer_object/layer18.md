## layer. setFiltersAtFrame()	

#### Availability

Adobe Animate 2020.

#### Usage

layer. setFiltersAtFrame (frameIndex,filterArray)	

#### Parameters

**frameIndex** – int, **filterArray** - The array of filters to be set

#### Returns

none	

#### Description

Sets filters at frame.

#### Example

The following example illustrates use of this method:


```javascript
var myFilters = an. getDocumentDOM(). getTimeline(). layers[0].getFiltersAtFrame(0);

an. getDocumentDOM(). getTimeline(). layers[0].setFiltersAtFrame(9,myFilters);
```