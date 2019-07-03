## tools summary

#### Availability

Flash MX 2004.

#### Description

The Tools object is accessible from the flash object ([fl.tools](#_bookmark550)). The [tools.toolObjs](#_bookmark1120) property contains an array of ToolObj objects, and the [tools.activeTool](#tools.activeTool) property returns the ToolObj object for the currently active tool. (See also [ToolObj object](#_bookmark1089) and the list of Extensible tools in [“Top-Level Functions and Methods” on page 18](#_bookmark13).)
>
***Note:** The following methods and properties are used only when creating extensible tools.*

#### Method summary

The following methods are available for the Tools object:

| **Method**                               | **Description**                                                                                                   |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [tools.constrainPoint()](#_bookmark1109) | Takes two points and returns a new adjusted or *constrained* point.                                               |
| [tools.getKeyDown()](#_bookmark1111)     | Returns the most recently pressed key.                                                                            |
| [tools.setCursor()](#_bookmark1116)      | Sets the pointer to a specified appearance.                                                                       |
| [tools.snapPoint()](#_bookmark1119)      | Takes a point as input and returns a new point that may be adjusted or *snapped* to the nearest geometric object. |

#### Property summary

The following properties are available for the Tools object:

| **Property**                          | **Description**                                                                            |
|---------------------------------------|--------------------------------------------------------------------------------------------|
| [tools.activeTool](#tools.activeTool) | Read-only; returns the [ToolObj object](#_bookmark1089) for the currently active tool.     |
| [tools.altIsDown](#_bookmark1108)     | Read-only; a Boolean value that identifies if the Alt key is being pressed.                |
| [tools.ctlIsDown](#_bookmark1110)     | Read-only; a Boolean value that identifies if the Control key is being pressed.            |
| [tools.mouseIsDown](#_bookmark1113)   | Read-only; a Boolean value that identifies if the left mouse button is currently pressed.  |
| [tools.penDownLoc](#_bookmark1114)    | Read-only; a point that represents the position of the last mouse-down event on the Stage. |
| [tools.penLoc](#_bookmark1115)        | Read-only; a point that represents the current location of the mouse.                      |
| [tools.shiftIsDown](#_bookmark1118)   | Read-only; a Boolean value that identifies if the Shift key is being pressed.              |
| [tools.toolObjs](#_bookmark1120)      | Read-only; an array of ToolObj objects.                                                    |

<span id="tools.activeTool" class="anchor"></span>

