## timeline.setLayerProperty()

#### Availability

Flash MX 2004.

#### Usage

timeline.setLayerProperty(property, value \[, layersToChange\])

#### Parameters

**property** A string that specifies the property to set. For a list of properties, see "[Layer object](../Layer_object/layer_summary.md)".
**value** The value to which you want to set the property. Use the same type of value you would use when setting the property in the layer object.
**layersToChange** A string that identifies which layers should be modified. Acceptable values are "selected", "all", and "others". The default value is "selected" if you omit this parameter. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; sets the specified property on all the selected layers to a specified value.

#### Example


The following example makes the selected layer(s) invisible:
```javascript
fl.getDocumentDOM().getTimeline().setLayerProperty("visible", false);
```
The following example sets the name of the selected layer(s) to selLayer:
```javascript
fl.getDocumentDOM().getTimeline().setLayerProperty("name", "selLayer");
```