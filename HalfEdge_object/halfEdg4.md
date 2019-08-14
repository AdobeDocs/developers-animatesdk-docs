## halfEdge.getVertex()

#### Availability

Flash MX 2004.

#### Usage

halfEdge.getVertex()

#### Parameters

None.

#### Returns

A [Vertex object](#!AdobeDocs/developers-animatesdk-docs/master/Vertex_object/vertex_summary.md)

#### Description

Method; gets the Vertex object at the head of the HalfEdge object. See [Vertex object](#!AdobeDocs/developers-animatesdk-docs/master/Vertex_object/vertex_summary.md)

#### Example

```javascript
The following example stores the Vertex object at the head of hEdge in the vertex variable:
var shape = fl.getDocumentDOM().selection\[0\]; var edge = shape.edges\[0\];
var hEdge = edge.getHalfEdge(0); var vertex = hEdge.getVertex();

```