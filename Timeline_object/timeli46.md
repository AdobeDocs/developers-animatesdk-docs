## timeline.setSelectedFrames()

#### Availability

Flash MX 2004.

#### Usage

timeline.setSelectedFrames(startFrameIndex, endFrameIndex \[, bReplaceCurrentSelection\]) timeline.setSelectedFrames(selectionList \[, bReplaceCurrentSelection\])

#### Parameters

**startFrameIndex** A zero-based index that specifies the beginning frame to set.
**endFrameIndex** A zero-based index that specifies the end of the selection; *endFrameIndex* is the frame after the last frame in the range to select.
**bReplaceCurrentSelection** A Boolean value that, if it is set to true, causes the currently selected frames to be deselected before the specified frames are selected. The default value is true.
**selectionList** An array of three integers, as returned by timeline.getSelectedFrames().

#### Returns

Nothing.

#### Description

Method; selects a range of frames in the current layer or sets the selected frames to the selection array passed into this method.

#### Example

```javascript
The following examples show two ways to select the top layer, Frame 1, up to but not including Frame 10, and then to add Frame 12 up to but not including Frame 15 on the same layer to the current selection (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().setSelectedFrames(0, 9);
fl.getDocumentDOM().getTimeline().setSelectedFrames(11, 14, false);
fl.getDocumentDOM().getTimeline().setSelectedFrames(\[0, 0, 9\]);
fl.getDocumentDOM().getTimeline().setSelectedFrames(\[0, 11, 14\], false);
The following example first stores the array of selected frames in the savedSelectionList variable and then uses the array later in the code to reselect those frames after a command or user interaction has changed the selection:
var savedSelectionList = fl.getDocumentDOM().getTimeline().getSelectedFrames();
// Do something that changes the selection. fl.getDocumentDOM().getTimeline().setSelectedFrames(savedSelectionList);

```
#### See also

[timeline.getSelectedFrames()](#!AdobeDocs/developers-animatesdk-docs/master/Timeline_object/timeli25.md)
