## contour.fill

#### Availability

Flash CS4 Professional.

#### Usage

contour.fill

#### Description

Property; a [Fill object](../Fill_object/fill_summary.md).

#### Example

Assuming that you have a contour with a fill selected, the following example displays the contour’s fill color in the Output panel:

```javascript
var insideContour = fl.getDocumentDOM().selection[0].contours[1];
var insideFill = insideContour.fill;
fl.trace(insideFill.color);
```