## timeline.cutLayers()

#### Availability

Flash CS5.5 Professional.

#### Usage

timeline.cutLayers(\[startLayerIndex \[, endLayerIndex\]\])

#### Parameters

**startLayerIndex** Optional. A zero-based index that specifies the beginning of the range of layers to cut. If you omit
startLayerIndex, the method uses the current selection.
**endLayerIndex** Optional. A zero-based index that specifies the layer at which to stop cutting. The range of layers to cut goes up to and including endLayerIndex. If you specify only startLayerIndex, then endLayerIndex defaults to the value of startLayerIndex.

#### Returns

Nothing.

#### Description

Method; Cuts the layers that are currently selected in the Timeline, or the layers in the specified range. Optional arguments can be provided in order to specify a layer or range of layers to cut.

#### Example

```
The following example cuts the layers from index 2 to index 7 in the Timeline:
fl.getDocumentDOM().getTimeline().cutLayers(2, 7);

```
#### See also

[timeline.copyLayers()](#_bookmark1039), [timeline.pasteLayers()](#_bookmark1070), [timeline.duplicateLayers()](#_bookmark1050)
