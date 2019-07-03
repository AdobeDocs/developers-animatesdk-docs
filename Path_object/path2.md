## path.addPoint()

#### Availability

Flash MX 2004.

#### Usage

path.addPoint(x, y)

#### Parameters

1.  A floating-point number that specifies the *x* position of the point.

2.  A floating-point number that specifies the *y* position of the point.

#### Returns

Nothing.

#### Description

Method; adds a point to the path.

#### Example

```
The following example creates a new path, stores it in the myPath variable, and assigns the new point to the path:
var myPath = fl.drawingLayer.newPath(); myPath.addPoint(10, 100);

```