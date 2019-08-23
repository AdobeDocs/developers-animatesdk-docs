## shape summary

**Inheritance** [Element object](#!AdobeDocs/developers-animatesdk-docs/test/Element_object/element_summary.md) \Shape object

#### Availability

Flash MX 2004.

#### Description

The Shape object is a subclass of the Element object. The Shape object provides more precise control than the drawing APIs when manipulating or creating geometry on the Stage. This control is necessary so that scripts can create useful effects and other drawing commands (see [Element object](#!AdobeDocs/developers-animatesdk-docs/test/Element_object/element_summary.md)).
All Shape methods and properties that change a shape or any of its subordinate parts must be placed between
[shape.beginEdit()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape.md)) and [shape.endEdit()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape4.md) calls to function correctly.

#### Method summary

In addition to the Element object methods, you can use the following methods with the Shape object:

| **Method**                                     | **Description**                                       |
|------------------------------------------------|-------------------------------------------------------|
| [shape.getCubicSegmentPoints()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape5.md) | Returns an array of points that define a cubic curve. |
| [shape.beginEdit()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape.md))        | Defines the start of an edit session.                 |
| [shape.deleteEdge()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape2.md)            | Deletes the specified edge.                           |
| [shape.endEdit()](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape4.md)               | Defines the end of an edit session for the shape.     |

#### Property summary

In addition to the Element object properties, the following properties are available for the Shape object:

| **Property**                             | **Description**                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [shape.contours](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape1.md)          | Read-only; an array of Contour objects for the shape (see [Contour object](#!AdobeDocs/developers-animatesdk-docs/test/Contour_object/contour_summary.md)).           |
| [shape.edges](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape3.md)             | Read-only; an array of Edge objects (see [Edge object](#!AdobeDocs/developers-animatesdk-docs/test/Edge_object/edge_summary.md)).                               |
| [shape.isDrawingObject](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape6.md)   | Read-only; if true, the shape is a drawing object.                                                    |
| [shape.isFloating](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape7.md)        | Read-only; if true, the shape is floating above the parent frame's (or group's) shape.                |
| [shape.isGroup](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape8.md)           | Read-only; if true, the shape is a group.                                                             |
| [shape.isOvalObject](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape9.md)      | Read-only; if true, the shape is a primitive Oval object (was created using the Oval tool).           |
| [shape.isRectangleObject](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape10.md) | Read-only; if true, the shape is a primitive Rectangle object (was created using the Rectangle tool). |
| [shape.members](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape11.md)           | An array of objects in the currently selected group.                                                  |
| [shape.numCubicSegments](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape12.md)  | Read-only; the number of cubic segments in the shape.                                                 |
| [shape.vertices](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape13.md)          | Read-only; an array of Vertex objects (see [Vertex object](#!AdobeDocs/developers-animatesdk-docs/test/Vertex_object/vertex_summary.md)).                          |

<span id="shape.beginEdit()" class="anchor"></span>

