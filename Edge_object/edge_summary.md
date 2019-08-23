## edge summary

#### Availability

Flash MX 2004.

#### Description

The Edge object represents an edge of a shape on the Stage.

#### Method summary

The following methods are available for the Edge object:

| **Method**                          | **Description**                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| [edge.getControl()](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge1.md)  | Gets a point object set to the location of the specified control point of the edge. |
| [edge.getHalfEdge()](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge2.md) | Returns a [HalfEdge object](#!AdobeDocs/developers-animatesdk-docs/master/HalfEdge_object/halfEdge_summary.md).                                         |
| [edge.setControl()](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge5.md)  | Sets the position of the control point of the edge.                                 |
| [edge.splitEdge()](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge6.md)   | Splits the edge into two pieces.                                                    |

#### Property summary

The following properties are available for the Edge object:

| **Property**                                      | **Description**                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [edge.cubicSegmentIndex](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge.md) | An integer that specifies the index value of a cubic segment of the edge. |
| [edge.id](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge3.md)                          | Read-only; an integer that represents a unique identifier for the edge.   |
| [edge.isLine](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge4.md)                      | Read-only; an integer with a value of 0 or 1.                             |
| [edge.stroke](#!AdobeDocs/developers-animatesdk-docs/master/Edge_object/edge7.md)                      | A [Stroke object](#!AdobeDocs/developers-animatesdk-docs/master/Stroke_object/stroke_summary.md).                                         |

<span id="edge.cubicSegmentIndex" class="anchor"></span>

