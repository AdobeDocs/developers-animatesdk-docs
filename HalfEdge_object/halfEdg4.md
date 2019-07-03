## halfEdge.getVertex()

#### Availability

Flash MX 2004.

#### Usage

halfEdge.getVertex()

#### Parameters

None.

#### Returns

A [Vertex object](#_bookmark1133)

#### Description

Method; gets the Vertex object at the head of the HalfEdge object. See [Vertex object](#_bookmark1133)

#### Example

```
The following example stores the Vertex object at the head of hEdge in the vertex variable:
var shape = fl.getDocumentDOM().selection\[0\]; var edge = shape.edges\[0\];
var hEdge = edge.getHalfEdge(0); var vertex = hEdge.getVertex();

```