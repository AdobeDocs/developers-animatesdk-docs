## halfEdge.getNext()

#### Availability

Flash MX 2004.

#### Usage

halfEdge.getNext()

#### Parameters

None.

#### Returns

A HalfEdge object.

#### Description

Method; gets the next half edge on the current contour.
>
***Note:** Although half edges have a direction and a sequence order, edges do not.*

#### Example

```
The following example stores the next half edge of the specified contour in the nextHalfEdge variable:
var shape = fl.getDocumentDOM().selection\[0\]; var hEdge = shape.edges\[0\].getHalfEdge( 0 ); var nextHalfEdge = hEdge.getNext();

```