## tools summary

#### Availability

Flash MX 2004.

#### Description

The Tools object is accessible from the flash object ([fl.tools](../flash_object_(fl)/fl76.md)/fl76.md)). The [tools.toolObjs](../Tools_object/tools11.md) property contains an array of ToolObj objects, and the [tools.activeTool](../Tools_object/tools.md) property returns the ToolObj object for the currently active tool. (See also [ToolObj object](../ToolObj_object/toolObj_summary.md) and the list of Extensible tools in ["Top-Level Functions and Methods" on page 18](../Top-Level_Functions_and_Methods/Top.md).)

***Note:** The following methods and properties are used only when creating extensible tools.*

#### Method summary

The following methods are available for the Tools object:

| **Method**                               | **Description**                                                                                                   |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [tools.constrainPoint()](../Tools_object/tools2.md) | Takes two points and returns a new adjusted or *constrained* point.                                               |
| [tools.getKeyDown()](../Tools_object/tools4.md)     | Returns the most recently pressed key.                                                                            |
| [tools.setCursor()](../Tools_object/tools8.md)      | Sets the pointer to a specified appearance.                                                                       |
| [tools.snapPoint()](../Tools_object/tools10.md)      | Takes a point as input and returns a new point that may be adjusted or *snapped* to the nearest geometric object. |

#### Property summary

The following properties are available for the Tools object:

| **Property**                          | **Description**                                                                            |
|---------------------------------------|--------------------------------------------------------------------------------------------|
| [tools.activeTool](../Tools_object/tools.md) | Read-only; returns the [ToolObj object](../ToolObj_object/toolObj_summary.md) for the currently active tool.     |
| [tools.altIsDown](../Tools_object/tools1.md)     | Read-only; a Boolean value that identifies if the Alt key is being pressed.                |
| [tools.ctlIsDown](../Tools_object/tools3.md)     | Read-only; a Boolean value that identifies if the Control key is being pressed.            |
| [tools.mouseIsDown](../Tools_object/tools5.md)   | Read-only; a Boolean value that identifies if the left mouse button is currently pressed.  |
| [tools.penDownLoc](../Tools_object/tools6.md)    | Read-only; a point that represents the position of the last mouse-down event on the Stage. |
| [tools.penLoc](../Tools_object/tools7.md)        | Read-only; a point that represents the current location of the mouse.                      |
| [tools.shiftIsDown](../Tools_object/tools9.md)   | Read-only; a Boolean value that identifies if the Shift key is being pressed.              |
| [tools.toolObjs](../Tools_object/tools11.md)      | Read-only; an array of ToolObj objects.                                                    |

<span id="tools.activeTool" class="anchor"></span>

