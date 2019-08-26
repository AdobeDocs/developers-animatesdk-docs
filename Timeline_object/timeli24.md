## timeline.getLayerProperty()

#### Availability

Flash MX 2004.

#### Usage

timeline.getLayerProperty(property)

#### Parameters

**property** A string that specifies the name of the property whose value you want to retrieve. For a list of properties, see the Property summary for the [Frame object](#!AdobeDocs/developers-animatesdk-docs/test/Frame_object/frame_summary.md).

#### Returns

The value of the specified property. Flash looks at the layer’s properties to determine the type. If all the specified layers don’t have the same property value, Flash returns undefined.

#### Description

Method; retrieves the specified property’s value for the selected layers.

#### Example

```javascript
The following example retrieves the name of the top layer in the current document and displays it in the Output panel:
fl.getDocumentDOM().getTimeline().currentLayer = 0;
var layerName = fl.getDocumentDOM().getTimeline().getLayerProperty("name"); fl.trace(layerName);

```