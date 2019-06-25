## edge summary

#### Availability

> Flash MX 2004.

#### Description

> The Edge object represents an edge of a shape on the Stage.

#### Method summary

> The following methods are available for the Edge object:

| **Method**                          | **Description**                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------|
| [edge.getControl()](#_bookmark366)  | Gets a point object set to the location of the specified control point of the edge. |
| [edge.getHalfEdge()](#_bookmark367) | Returns a [HalfEdge object](#_bookmark644).                                         |
| [edge.setControl()](#_bookmark370)  | Sets the position of the control point of the edge.                                 |
| [edge.splitEdge()](#_bookmark371)   | Splits the edge into two pieces.                                                    |

#### Property summary

> The following properties are available for the Edge object:

| **Property**                                      | **Description**                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [edge.cubicSegmentIndex](#edge.cubicSegmentIndex) | An integer that specifies the index value of a cubic segment of the edge. |
| [edge.id](#_bookmark368)                          | Read-only; an integer that represents a unique identifier for the edge.   |
| [edge.isLine](#_bookmark369)                      | Read-only; an integer with a value of 0 or 1.                             |
| [edge.stroke](#_bookmark372)                      | A [Stroke object](#_bookmark876).                                         |

<span id="edge.cubicSegmentIndex" class="anchor"></span>
