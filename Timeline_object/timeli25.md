## timeline.getSelectedFrames()

#### Availability

Flash MX 2004.

#### Parameters

None.

#### Returns

An array containing 3*n* integers, where *n* is the number of selected regions. The first integer in each group is the layer index, the second integer is the start frame of the beginning of the selection, and the third integer specifies the ending frame of that selection range. The ending frame is not included in the selection.

#### Description

Method; retrieves the currently selected frames in an array.

#### Example

```javascript
With the top layer being the current layer, the following example displays 0,5,10,0,20,25 in the Output panel:
var timeline = fl.getDocumentDOM().getTimeline(); timeline.setSelectedFrames(5,10); timeline.setSelectedFrames(20,25,false);
var theSelectedFrames = timeline.getSelectedFrames(); fl.trace(theSelectedFrames);

```
#### See also

[timeline.setSelectedFrames()](../Timeline_object/timeli46.md)
