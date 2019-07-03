## shape summary

**Inheritance** [Element object](#_bookmark374) \Shape object

#### Availability

Flash MX 2004.

#### Description

The Shape object is a subclass of the Element object. The Shape object provides more precise control than the drawing APIs when manipulating or creating geometry on the Stage. This control is necessary so that scripts can create useful effects and other drawing commands (see [Element object](#_bookmark374)).
>
All Shape methods and properties that change a shape or any of its subordinate parts must be placed between
>
[shape.beginEdit()](#shape.beginEdit()) and [shape.endEdit()](#_bookmark812) calls to function correctly.

#### Method summary

In addition to the Element object methods, you can use the following methods with the Shape object:

| **Method**                                     | **Description**                                       |
|------------------------------------------------|-------------------------------------------------------|
| [shape.getCubicSegmentPoints()](#_bookmark813) | Returns an array of points that define a cubic curve. |
| [shape.beginEdit()](#shape.beginEdit())        | Defines the start of an edit session.                 |
| [shape.deleteEdge()](#_bookmark810)            | Deletes the specified edge.                           |
| [shape.endEdit()](#_bookmark812)               | Defines the end of an edit session for the shape.     |

#### Property summary

In addition to the Element object properties, the following properties are available for the Shape object:

| **Property**                             | **Description**                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [shape.contours](#_bookmark809)          | Read-only; an array of Contour objects for the shape (see [Contour object](#_bookmark109)).           |
| [shape.edges](#_bookmark811)             | Read-only; an array of Edge objects (see [Edge object](#_bookmark362)).                               |
| [shape.isDrawingObject](#_bookmark815)   | Read-only; if true, the shape is a drawing object.                                                    |
| [shape.isFloating](#_bookmark817)        | Read-only; if true, the shape is floating above the parent frame's (or group's) shape.                |
| [shape.isGroup](#_bookmark818)           | Read-only; if true, the shape is a group.                                                             |
| [shape.isOvalObject](#_bookmark819)      | Read-only; if true, the shape is a primitive Oval object (was created using the Oval tool).           |
| [shape.isRectangleObject](#_bookmark821) | Read-only; if true, the shape is a primitive Rectangle object (was created using the Rectangle tool). |
| [shape.members](#_bookmark823)           | An array of objects in the currently selected group.                                                  |
| [shape.numCubicSegments](#_bookmark824)  | Read-only; the number of cubic segments in the shape.                                                 |
| [shape.vertices](#_bookmark825)          | Read-only; an array of Vertex objects (see [Vertex object](#_bookmark1133)).                          |

<span id="shape.beginEdit()" class="anchor"></span>

