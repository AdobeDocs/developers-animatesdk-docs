## path.addCubicCurve()

#### Availability

Flash MX 2004.

#### Usage

path.addCubicCurve(xAnchor, yAnchor, x2, y2, x3, y3, x4, y4)

#### Parameters

**xAnchor** A floating-point number that specifies the *x* position of the first control point. **yAnchor** A floating-point number that specifies the *y* position of the first control point. **x2** A floating-point number that specifies the *x* position of the second control point.
**y2** A floating-point number that specifies the *y* position of the second control point. **x3** A floating-point number that specifies the *x* position of the third control point. **y3** A floating-point number that specifies the *y* position of the third control point. **x4** A floating-point number that specifies the *x* position of the fourth control point. **y4** A floating-point number that specifies the *y* position of the fourth control point.

#### Returns

Nothing.

#### Description

Method; appends a cubic Bézier curve segment to the path.

#### Example

```
The following example creates a new path, stores it in the myPath variable, and assigns the curve to the path:
var myPath = fl.drawingLayer.newPath(); myPath.addCubicCurve(0, 0, 10, 20, 20, 20, 30, 0);

```