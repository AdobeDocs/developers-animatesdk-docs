## path summary

#### Availability

> Flash MX 2004.

#### Description

> The Path object defines a sequence of line segments (straight, curved, or both), which you typically use when creating extensible tools. The following example shows an instance of a Path object being returned from the flash object:
>
> path = fl.drawingLayer.newPath();
>
> See also the [drawingLayer object](#_bookmark345).

#### Method summary

> The following methods are available for the Path object:

| **Method**                                    | **Description**                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [path.addCubicCurve()](#path.addCubicCurve()) | Appends a cubic Bézier curve segment to the path.                                                                         |
| [path.addCurve()](#_bookmark762)              | Appends a quadratic Bézier segment to the path.                                                                           |
| [path.addPoint()](#_bookmark763)              | Adds a point to the path.                                                                                                 |
| [path.clear()](#_bookmark764)                 | Removes all points from the path.                                                                                         |
| [path.close()](#_bookmark765)                 | Appends a point at the location of the first point of the path and extends the path to that point, which closes the path. |
| [path.makeShape()](#_bookmark766)             | Creates a shape on the Stage by using the current stroke and fill settings.                                               |
| [path.newContour()](#_bookmark767)            | Starts a new contour in the path.                                                                                         |

#### Property summary

> The following properties are available for the Path object:

| **Property**               | **Description**                                                      |
|----------------------------|----------------------------------------------------------------------|
| [path.nPts](#_bookmark768) | Read-only; an integer representing the number of points in the path. |

<span id="path.addCubicCurve()" class="anchor"></span>
