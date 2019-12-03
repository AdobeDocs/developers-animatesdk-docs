## vertex.x

#### Availability

Flash MX 2004.

#### Usage

*vertex.x*

#### Description

Read-only property; the *x* location of the vertex, in pixels.

#### Example

The following example displays the location of the *x* and *y* values of the vertex in the Output panel:

```javascript
var shape = fl.getDocumentDOM().selection[0]; 
var hEdge = shape.edges[0].getHalfEdge(0); 
var vertex = hEdge.getVertex();

fl.trace('x location of vertex is: ' + vertex.x); 
fl.trace('y location of vertex is: ' + vertex.y);

```