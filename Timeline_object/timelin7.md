## timeline.copyLayers()

#### Availability

Flash CS5.5 Professional.

#### Usage

timeline.copyLayers(\[startLayerIndex \[, endLayerIndex\]\])

#### Parameters

**startLayerIndex** Optional. A zero-based index that specifies the beginning of the range of layers to copy. If you omit
startLayerIndex, the method uses the current selection.
**endLayerIndex** Optional. A zero-based index that specifies the layer at which to stop copying. The range of layers to copy goes up to and including endLayerIndex. If you specify only startLayerIndex, then endLayerIndex defaults to the value of startLayerIndex.

#### Returns

Nothing.

#### Description

Method; Copies the layers that are currently selected in the Timeline, or the layers in the specified range. Optional arguments can be provided in order to specify a layer or range of layers to copy.

#### Example

```javascript
The following example copies the layers from index 2 to index 7 in the Timeline:
fl.getDocumentDOM().getTimeline().copyLayers(2, 7);

```
#### See also

[timeline.cutLayers()](#!AdobeDocs/developers-animatesdk-docs/master/Timeline_object/timeli15.md), [timeline.pasteLayers()](#!AdobeDocs/developers-animatesdk-docs/master/Timeline_object/timeli35.md), [timeline.duplicateLayers()](#!AdobeDocs/developers-animatesdk-docs/master/Timeline_object/timeli17.md)
