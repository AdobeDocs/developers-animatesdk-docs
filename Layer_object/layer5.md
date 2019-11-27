## layer.layerType

#### Availability

Flash MX 2004.

#### Usage

layer.layerType

#### Description

Property; a string that specifies the current use of the layer; equivalent to the Type setting in the Layer Properties dialog box. Acceptable values are "normal", "guide", "guided", "mask", "masked", and "folder".

#### Example

```javascript
The following example sets the first layer in the timeline to type folder:

fl.getDocumentDOM().getTimeline().layers[0].layerType = "folder";

```