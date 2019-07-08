## drawingLayer.curveTo()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.curveTo(xCtl, yCtl, xEnd, yEnd)

#### Parameters

**xCtl** A floating-point value that is the *x* position of the control point.
**yCtl** A floating-point value that is the *y* position of the control point. **xEnd** A floating-point value that is the *x* position of the end control point. **yEnd** A floating-point value that is the *y* position of the end control point.

#### Returns

Nothing.

#### Description

Method; draws a quadratic curve segment starting at the current drawing position and ending at a specified point. You typically use this method only when creating extensible tools.

#### Example

```javascript
The following example draws a quadratic curve using the specified control points:
fl.drawingLayer.curveTo(0, 0, 2, 0);

```