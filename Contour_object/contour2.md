## contour.interior

#### Availability

Flash MX 2004.

#### Usage

contour.interior

#### Description

Read-only property; the value is true if the contour encloses an area; false otherwise.

#### Example

This example traverses all the contours of the selected shape and shows the value of the interior property for each contour in the Output panel:

```javascript
var elt = fl.getDocumentDOM().selection[0];
elt.beginEdit();
var contourArray = elt.contours;
var contourCount = 0;
for (i=0;i<contourArray.length;i++) {
var contour = contourArray[i];
fl.trace("Next Contour, interior:" + contour.interior );
contourCount++;
}
elt.endEdit();
```