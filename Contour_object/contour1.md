## contour.getHalfEdge()

#### Availability

Flash MX 2004.

#### Usage

contour.getHalfEdge()

#### Parameters

None.

#### Returns

A [HalfEdge object](#_bookmark644).

#### Description

Method; returns a [HalfEdge object](#_bookmark644) on the contour of the selection.

#### Example

```javascript
This example traverses all the contours of the selected shape and shows the coordinates of the vertices in the Output panel:
// with a shape selected
var elt = fl.getDocumentDOM().selection\[0\]; elt.beginEdit();
var contourArray = elt.contours; var contourCount = 0;
for (i=0;i\<contourArray.length;i++)
{
var contour = contourArray\[i\]; contourCount++;
var he = contour.getHalfEdge();
var iStart = he.id; var id = 0;
while (id != iStart)
{
// Get the next vertex. var vrt = he.getVertex();
var x = vrt.x; var y = vrt.y;
fl.trace("vrt: " + x + ", " + y);
he = he.getNext(); id = he.id;
}
}
elt.endEdit();

```