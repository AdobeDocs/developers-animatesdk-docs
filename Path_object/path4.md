## path.close()

#### Availability

Flash MX 2004.

#### Usage

path.close()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; appends a point at the location of the first point of the path and extends the path to that point, which closes the path. If the path has no points, no points are added.

#### Example

```
The following example creates a closed path:
var myPath = fl.drawingLayer.newPath(); myPath.close();

```