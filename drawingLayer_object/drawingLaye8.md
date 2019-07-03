## drawingLayer.moveTo()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.moveTo(x, y)

#### Parameters

**x** A floating-point value that specifies the *x* coordinate of the position at which to start drawing.
**y** A floating-point value that specifies the *y* coordinate of the position at which to start drawing.

#### Returns

Nothing.

#### Description

Method; sets the current drawing position. You typically use this method only when creating extensible tools.

#### Example

```
The following example sets the current drawing position at the point (10,15):
fl.drawingLayer.moveTo(10, 15);

```