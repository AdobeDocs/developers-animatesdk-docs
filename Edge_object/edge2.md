## edge.getHalfEdge()

#### Availability

Flash MX 2004.

#### Usage

edge.getHalfEdge(index)

#### Parameters

**index** An integer that specifies which half edge to return. The value of *index* must be either 0 for the first half edge or 1 for the second half edge.

#### Returns

A HalfEdge object.

#### Description

Method; returns a [HalfEdge object](../HalfEdge_object/halfEdge_summary.md).

#### Example

The following example stores the half edges of the specified edge in the hEdge0 and hEdge1 variables:
```javascript
var shape = fl.getDocumentDOM().selection[0];
var edge = shape.edges[0];
var hEdge0 = edge.getHalfEdge(0);
var hEdge1 = edge.getHalfEdge(1);

```