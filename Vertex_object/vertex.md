## vertex.getHalfEdge()

#### Availability

Flash MX 2004.

#### Usage

vertex.getHalfEdge()

#### Parameters

None.

#### Returns

A [HalfEdge object](#_bookmark644).

#### Description

Method; gets a [HalfEdge object](#_bookmark644) that shares this vertex.

#### Example

```
The following example shows how to get other half edges that share the same vertex:
var shape = fl.getDocumentDOM().selection\[0\]; var hEdge = shape.edges\[0\].getHalfEdge(0); var theVertex = hEdge.getVertex();
var someHEdge = theVertex.getHalfEdge(); // Not necessarily the same half edge var theSameVertex = someHEdge.getVertex();
fl.trace('the same vertex: ' + theSameVertex);

```