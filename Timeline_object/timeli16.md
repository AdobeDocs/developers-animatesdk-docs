## timeline.deleteLayer()

#### Availability

Flash MX 2004.

#### Usage

timeline.deleteLayer(\[index\])

#### Parameters

**index** A zero-based index that specifies the layer to be deleted. If there is only one layer in the timeline, this method has no effect. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; deletes a layer. If the layer is a folder, all layers within the folder are deleted. If you do not specify the layer index, Flash deletes the currently selected layers.

#### Example

```javascript
The following example deletes the second layer from the top: fl.getDocumentDOM().getTimeline().deleteLayer(1); The following example deletes the currently selected layers: fl.getDocumentDOM().getTimeline().deleteLayer();

```