## shape.vertices

#### Availability

Flash MX 2004.

#### Usage

shape.vertices

#### Description

Read-only property; an array of Vertex objects (see [Vertex object](#!AdobeDocs/developers-animatesdk-docs/test/Vertex_object/vertex_summary.md)).

#### Example

```javascript
The following example stores the first selected object in the someShape variable, and then shows the number of vertices for that object in the Output panel:
var someShape = fl.getDocumentDOM().selection\[0\];
fl.trace("The shape has " + someShape.vertices.length + " vertices.");

```