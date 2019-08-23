## stroke.shapeFill

#### Availability

Flash 8.

#### Usage

stroke.shapeFill

#### Description

Property; a [Fill object](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill_summary.md) that represents the fill settings of the stroke.

#### Example

```javascript
The following example specifies fill settings and then applies them to the stroke:
var fill = fl.getDocumentDOM().getCustomFill(); fill.linearGradient = true;
fill.colorArray = \[ 00ff00, ff0000, fffff \];
var stroke = fl.getDocumentDOM().getCustomStroke(); stroke.shapeFill = fill; fl.getDocumentDOM().setCustomStroke(stroke);

```