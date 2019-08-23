## path summary

#### Availability

Flash MX 2004.

#### Description

The Path object defines a sequence of line segments (straight, curved, or both), which you typically use when creating extensible tools. The following example shows an instance of a Path object being returned from the flash object:
path = fl.drawingLayer.newPath();
See also the [drawingLayer object](#!AdobeDocs/developers-animatesdk-docs/master/drawingLayer_object/drawingLayersummary.md).

#### Method summary

The following methods are available for the Path object:

| **Method**                                    | **Description**                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [path.addCubicCurve()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path.md)) | Appends a cubic Bézier curve segment to the path.                                                                         |
| [path.addCurve()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path1.md)              | Appends a quadratic Bézier segment to the path.                                                                           |
| [path.addPoint()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path2.md)              | Adds a point to the path.                                                                                                 |
| [path.clear()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path3.md)                 | Removes all points from the path.                                                                                         |
| [path.close()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path4.md)                 | Appends a point at the location of the first point of the path and extends the path to that point, which closes the path. |
| [path.makeShape()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path5.md)             | Creates a shape on the Stage by using the current stroke and fill settings.                                               |
| [path.newContour()](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path6.md)            | Starts a new contour in the path.                                                                                         |

#### Property summary

The following properties are available for the Path object:

| **Property**               | **Description**                                                      |
|----------------------------|----------------------------------------------------------------------|
| [path.nPts](#!AdobeDocs/developers-animatesdk-docs/master/Path_object/path7.md) | Read-only; an integer representing the number of points in the path. |

<span id="path.addCubicCurve()" class="anchor"></span>

