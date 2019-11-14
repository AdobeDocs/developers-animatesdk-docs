## halfEdge.getEdge()

#### Availability

Flash MX 2004.

#### Usage

halfEdge.getEdge()

#### Parameters

None.

#### Returns

An [Edge object](../Edge_object/edge_summary.md).

#### Description

Method; gets the Edge object for the HalfEdge object. See [Edge object](../Edge_object/edge_summary.md).

#### Example

```javascript
The following example illustrates getting an edge and a half edge for the specified shape:
var shape = fl.getDocumentDOM().selection\[0\]; var hEdge = shape.edges\[0\].getHalfEdge(0); var edge = hEdge.getEdge();

```