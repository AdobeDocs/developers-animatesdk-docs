## halfEdge.getPrev()

#### Availability

Flash MX 2004.

#### Usage

halfEdge.getPrev()

#### Parameters

None.

#### Returns

A HalfEdge object.

#### Description

Method; gets the preceding HalfEdge object on the current contour.
***Note:** Although half edges have a direction and a sequence order, edges do not.*

#### Example

```javascript
The following example stores the previous half edge of the specified contour in the prevHalfEdge variable:
var shape = fl.getDocumentDOM().selection[0]; var hEdge = shape.edges[0].getHalfEdge( 0 ); var prevHalfEdge = hEdge.getPrev();

```