## vertex.setLocation()

#### Availability

Flash MX 2004.

#### Usage

vertex.setLocation(x, y)

#### Parameters

1.  A floating-point value that specifies the *x* coordinate of where the vertex should be positioned, in pixels.

2.  A floating-point value that specifies the *y* coordinate of where the vertex should be positioned, in pixels.

#### Returns

Nothing.

#### Description

Method; sets the location of the vertex. You must call [shape.beginEdit()](#!AdobeDocs/developers-animatesdk-docs/master/Shape_object/shape.md) before using this method.

#### Example

```javascript
The following example sets the vertex to the origin point:
var shape = fl.getDocumentDOM().selection\[0\]; shape.beginEdit();
var hEdge = shape.edges\[0\].getHalfEdge(0); var vertex = hEdge.getVertex();
var someHEdge = vertex.getHalfEdge(); var vertex = someHEdge.getVertex();
// Move the vertex to the origin. vertex.setLocation(0.0, 0.0); shape.endEdit();

```