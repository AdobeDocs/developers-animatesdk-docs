## layer.color

#### Availability

Flash MX 2004.

#### Usage

layer.color

#### Description

Property; the color assigned to outline the layer, in one of the following formats:

-   A string in the format "#RRGGBB" or "#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

This property is equivalent to the Outline color setting in the Layer Properties dialog box.

#### Example

The following example stores the value of the first layer in the colorValue variable: var colorValue = 

```javascript
var colorValue = fl.getDocumentDOM().getTimeline().layers[0].color;
```
The following example shows three ways to set the color of the first layer to red:
```javascript

fl.getDocumentDOM().getTimeline().layers[0].color=16711680;
fl.getDocumentDOM().getTimeline().layers[0].color="#ff0000";
fl.getDocumentDOM().getTimeline().layers[0].color=0xFF0000;
```