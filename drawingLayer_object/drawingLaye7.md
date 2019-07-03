## drawingLayer.lineTo()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.lineTo(x, y)

#### Parameters

**x** A floating-point value that is the *x* coordinate of the end point of the line to draw.
>
**y** A floating-point value that is the *y* coordinate of the end point of the line to draw.

#### Returns

Nothing.

#### Description

Method; draws a line from the current drawing position to the point (*x,y*). You typically use this method only when creating extensible tools.

#### Example

```
The following example draws a line from the current drawing position to the point (20,30):
fl.drawingLayer.lineTo(20, 30);

```