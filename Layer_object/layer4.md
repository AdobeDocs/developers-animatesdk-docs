## layer.height

#### Availability

Flash MX 2004.

#### Usage

layer.height

#### Description

Property; an integer that specifies the percentage layer height; equivalent to the Layer height value in the Layer Properties dialog box. Acceptable values represent percentages of the default height: 100, 200, or 300.

#### Example

The following example stores the percentage value of the first layer’s height setting:

```javascript
var layerHeight = fl.getDocumentDOM().getTimeline().layers[0].height;
```

The following example sets the height of the first layer to 300 percent:

```javascript
fl.getDocumentDOM().getTimeline().layers[0].height = 300;
```