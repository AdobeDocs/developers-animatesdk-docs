## halfEdge summary

#### Availability

> Flash MX 2004.

#### Description

> The HalfEdge object is the directed side of the edge of a [Shape object](#_bookmark805). An edge has two half edges. You can transverse the contours of a shape by “walking around” these half edges. For example, starting from a half edge, you can trace all the half edges around a contour of a shape, and return to the original half edge.
>
> Half edges are ordered. One half edge represents one side of the edge; the other half edge represents the other side.

#### Method summary

> The following methods are available for the HalfEdge object:

| **Method**                                      | **Description**                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------|
| [halfEdge.getEdge()](#halfEdge.getEdge())       | Gets the [Edge object](#_bookmark362) for the HalfEdge object.               |
| [halfEdge.getNext()](#_bookmark647)             | Gets the next half edge on the current contour.                              |
| [halfEdge.getOppositeHalfEdge()](#_bookmark648) | Gets the HalfEdge object on the other side of the edge.                      |
| [halfEdge.getPrev()](#_bookmark649)             | Gets the preceding HalfEdge object on the current contour.                   |
| [halfEdge.getVertex()](#_bookmark650)           | Gets the [Vertex object](#_bookmark1133) at the head of the HalfEdge object. |

#### Property summary

> The following properties are available for the HalfEdge object:

| **Property**                 | **Description**                                                 |
|------------------------------|-----------------------------------------------------------------|
| [halfEdge.id](#_bookmark651) | Read-only; a unique integer identifier for the HalfEdge object. |

<span id="halfEdge.getEdge()" class="anchor"></span>
