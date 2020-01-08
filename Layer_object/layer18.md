## layer. setFiltersAtFrame()	

#### Availability

Animate 2020.

#### Usage

layer. setFiltersAtFrame (frameIndex,filterArray)	

#### Parameters

**frameIndex** – It is an integer that specifies absolute frame index.
**filterArray** - The array of filters to be set

#### Returns

none	

#### Description

Method; Apply filters at a particular frame.

#### Example

The following example illustrates use of this method:

```javascript
var myFilters = an. getDocumentDOM(). getTimeline(). layers[0].getFiltersAtFrame(0);

an. getDocumentDOM(). getTimeline(). layers[0].setFiltersAtFrame(9,myFilters);
```