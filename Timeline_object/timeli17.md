## timeline.duplicateLayers()

#### Availability

Flash CS5.5 Professional.

#### Usage

timeline.duplicateLayers(\[startLayerIndex \[, endLayerIndex\]\])

#### Parameters

**startLayerIndex** Optional. A zero-based index that specifies the beginning of the range of layers to copy. It also specifies the layer above which the layers on the clipboard are pasted. If you omit startLayerIndex, the method uses the current layer selection.
**endLayerIndex** Optional. A zero-based index that specifies the layer at which to stop copying. The range of layers to copy goes up to and including endLayerIndex. If you specify only startLayerIndex, then endLayerIndex defaults to the value of startLayerIndex.

#### Returns

Nothing.

#### Description

Method; Duplicates the layers that are currently selected in the Timeline, or the layers in the specified range. Optional arguments can be provided in order to specify a layer or range of layers to duplicate.

#### Example

```javascript
The following example duplicates the layer currently selected in the Timeline:
fl.getDocumentDOM().getTimeline().duplicateLayers();
The following example duplicates the layers from index 2 to index 7 above layer index 2:
fl.getDocumentDOM().getTimeline().duplicatedLayers(2,7);

```
#### See also

[timeline.copyLayers()](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timelin7.md), [timeline.cutLayers()](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeli15.md), [timeline.pasteLayers()](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeli35.md)
