## drawingLayer.setColor()

#### Availability

Flash MX 2004.

#### Usage

drawingLayer.setColor(color)

#### Parameters

**color** The color of subsequently drawn data, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

#### Returns

Nothing.

#### Description

Method; sets the color of subsequently drawn data. Applies only to persistent data. To use this method, the parameter passed to drawingLayer.beginDraw() must be set to true. You typically use this method only when creating extensible tools. See [drawingLayer.beginDraw()](#_bookmark347).

#### Example

```javascript
The following example draws a red line on the Stage:
fl.drawingLayer.beginDraw( true ); fl.drawingLayer.beginFrame(); fl.drawingLayer.setColor( "\#ff0000" ); fl.drawingLayer.moveTo(0,0); fl.drawingLayer.lineTo(100,100); fl.drawingLayer.endFrame(); fl.drawingLayer.endDraw();

```