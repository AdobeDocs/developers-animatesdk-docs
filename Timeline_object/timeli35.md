## timeline.pasteLayers()

#### Availability

Flash CS5.5 Professional.

#### Usage

timeline.pasteLayers(\[layerIndex\])

#### Parameters

**layerIndex** Optional. A zero-based index that specifies the layer above which the layers on the clipboard are pasted. If you omit layerIndex, the method uses the current selection.

#### Returns

Integer indicating the lowest layer index of the layers that were pasted.

#### Description

Method; Paste layers that have been previously cut or copied above the currently selected layer, or above the specified layer index. If the specified layer is a folder layer, the layers are pasted into the folder. Returns the lowest layer index of the layers that were pasted. This action does not affect the system clipboard.

#### Example

```
The following example pastes the layers from the layer clipboard above the currently selected layer in the Timeline:
fl.getDocumentDOM().getTimeline().pasteLayers();
The following example pastes the layers from the layer clipboard above layer index 2:
fl.getDocumentDOM().getTimeline().pasteLayers(2);

```
#### See also

[timeline.cutLayers()](#_bookmark1048), [timeline.copyLayers()](#_bookmark1039), [timeline.duplicateLayers()](#_bookmark1050)
