## drawingLayersummary

#### Availability

Flash MX 2004.

#### Description

The drawingLayer object is accessible from JavaScript as a child of the flash object. The drawingLayer object is used for extensible tools when the user wants to temporarily draw while dragging—for example, when creating a selection marquee. You should call [drawingLayer.beginFrame()](#_bookmark348) before you call any other drawingLayer methods.

#### Method summary

The following methods are available for the drawingLayer object:

| **Method**                                            | **Description**                                                                                                 |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [drawingLayer.beginDraw()](#drawingLayer.beginDraw()) | Puts Flash in drawing mode.                                                                                     |
| [drawingLayer.beginFrame()](#_bookmark348)            | Erases what was previously drawn using the drawingLayer and prepares for more drawing commands.                 |
| [drawingLayer.cubicCurveTo()](#_bookmark349)          | Draws a cubic curve from the current pen location using the parameters as the coordinates of the cubic segment. |
| [drawingLayer.curveTo()](#_bookmark350)               | Draws a quadratic curve segment starting at the current drawing position and ending at a specified point.       |
| [drawingLayer.drawPath()](#_bookmark351)              | Draws the specified path.                                                                                       |
| [drawingLayer.endDraw()](#_bookmark352)               | Exits drawing mode.                                                                                             |
| [drawingLayer.endFrame()](#_bookmark353)              | Signals the end of a group of drawing commands.                                                                 |
| [drawingLayer.lineTo()](#_bookmark354)                | Draws a line from the current drawing position to the point (*x,y*).                                            |
| [drawingLayer.moveTo()](#_bookmark355)                | Sets the current drawing position.                                                                              |
| [drawingLayer.newPath()](#_bookmark356)               | Returns a new [Path object](#_bookmark759).                                                                     |
| [drawingLayer.setColor()](#_bookmark357)              | Sets the color of subsequently drawn data.                                                                      |
| [drawingLayer.setFill()](#_bookmark359)               | This method is not available.                                                                                   |
| [drawingLayer.setStroke()](#_bookmark360)             | This method is not available.                                                                                   |

<span id="drawingLayer.beginDraw()" class="anchor"></span>

