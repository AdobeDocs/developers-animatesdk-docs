## timeline.findLayerIndex()

#### Availability

Flash MX 2004.

#### Usage

timeline.findLayerIndex(name)

#### Parameters

**name** A string that specifies the name of the layer to find.

#### Returns

An array of index values for the specified layer. If the specified layer is not found, Flash returns undefined.

#### Description

Method; finds an array of indexes for the layers with the given name. The layer index is flat, so folders are considered part of the main index.

#### Example

```javascript
The following example shows the index values of all layers named Layer 7 in the Output panel:
var layerIndex = fl.getDocumentDOM().getTimeline().findLayerIndex("Layer 7"); fl.trace(layerIndex);
The following example illustrates how to pass the values returned from this method back to
[timeline.setSelectedLayers()](#_bookmark1084):
var layerIndex = fl.getDocumentDOM().getTimeline().findLayerIndex("Layer 1"); fl.getDocumentDOM().getTimeline().setSelectedLayers(layerIndex\[0\], true);

```