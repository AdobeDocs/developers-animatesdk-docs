## drawingLayer.beginDraw()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.beginDraw(\[persistentDraw\])

#### Parameters

**persistentDraw** A Boolean value (optional). If set to true, it indicates that the drawing in the last frame remains on the Stage until a new beginDraw() or beginFrame() call is made. (In this context, *frame* refers to where you start and end drawing; it does not refer to timeline frames.) For example, when users draw a rectangle, they can preview the outline of the shape while dragging the mouse. If you want that preview shape to remain after the user releases the mouse button, set *persistentDraw* to true.

#### Returns

Nothing.

#### Description

Method; puts Flash in drawing mode. Drawing mode is used for temporary drawing while the mouse button is pressed. You typically use this method only when creating extensible tools.

#### Example

```javascript
The following example puts Flash in drawing mode:
fl.drawingLayer.beginDraw();

```