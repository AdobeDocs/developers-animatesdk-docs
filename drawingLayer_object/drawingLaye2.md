## drawingLayer.cubicCurveTo()

#### Availability

Flash MX 2004.

#### Usage

*drawingLayer.cubicCurveTo(x1Ctrl, y1Ctrl, x2Ctl, y2Ctl, xEnd, yEnd)*

#### Parameters

**x1Ctl** A floating-point value that is the *x* location of the first control point. 

**y1Ctl** A floating-point value that is the *y* location of the first control point. 

**x2Ctl** A floating-point value that is the *x* position of the middle control point.

**y2Ctl** A floating-point value that is the *y* position of the middle control point.

**xEnd** A floating-point value that is the *x* position of the end control point. 

**yEnd** A floating-point value that is the *y* position of the end control point.

#### Returns

Nothing.

#### Description

Method; draws a cubic curve from the current pen location using the parameters as the coordinates of the cubic segment. You typically use this method only when creating extensible tools.

#### Example

```javascript
The following example draws a cubic curve using the specified control points:
fl.drawingLayer.cubicCurveTo(0, 0, 1, 1, 2, 0);

```