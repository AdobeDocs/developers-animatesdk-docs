## drawingLayersummary

#### Availability

Flash MX 2004.

#### Description

The drawingLayer object is accessible from JavaScript as a child of the flash object. The drawingLayer object is used for extensible tools when the user wants to temporarily draw while dragging—for example, when creating a selection marquee. You should call [drawingLayer.beginFrame()](../drawingLayer_object/drawingLaye1.md) before you call any other drawingLayer methods.

#### Method summary

The following methods are available for the drawingLayer object:

| **Method**                                            | **Description**                                                                                                 |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [drawingLayer.beginDraw()](../drawingLayer_object/drawingLayer.md) | Puts Flash in drawing mode.                                                                                     |
| [drawingLayer.beginFrame()](../drawingLayer_object/drawingLaye1.md)            | Erases what was previously drawn using the drawingLayer and prepares for more drawing commands.                 |
| [drawingLayer.cubicCurveTo()](../drawingLayer_object/drawingLaye2.md)          | Draws a cubic curve from the current pen location using the parameters as the coordinates of the cubic segment. |
| [drawingLayer.curveTo()](../drawingLayer_object/drawingLaye3.md)               | Draws a quadratic curve segment starting at the current drawing position and ending at a specified point.       |
| [drawingLayer.drawPath()](../drawingLayer_object/drawingLaye4.md)              | Draws the specified path.                                                                                       |
| [drawingLayer.endDraw()](../drawingLayer_object/drawingLaye5.md)               | Exits drawing mode.                                                                                             |
| [drawingLayer.endFrame()](../drawingLayer_object/drawingLaye6.md)              | Signals the end of a group of drawing commands.                                                                 |
| [drawingLayer.lineTo()](../drawingLayer_object/drawingLaye7.md)                | Draws a line from the current drawing position to the point (*x,y*).                                            |
| [drawingLayer.moveTo()](../drawingLayer_object/drawingLaye8.md)                | Sets the current drawing position.                                                                              |
| [drawingLayer.newPath()](../drawingLayer_object/drawingLaye9.md)               | Returns a new [Path object](../Path_object/path_summary.md).                                                                     |
| [drawingLayer.setColor()](../drawingLayer_object/drawingLay10.md)              | Sets the color of subsequently drawn data.                                                                      |
| [drawingLayer.setFill()](../drawingLayer_object/drawingLay11.md)               | This method is not available.                                                                                   |
| [drawingLayer.setStroke()](../drawingLayer_object/drawingLay12.md)             | This method is not available.                                                                                   |

<span id="drawingLayer.beginDraw()" class="anchor"></span>

