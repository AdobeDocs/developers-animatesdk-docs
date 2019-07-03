## toolObj summary

#### Availability

Flash MX 2004.

#### Description

A ToolObj object represents an individual tool in the Tools panel. To access a ToolObj object, use properties of the [Tools object](#_bookmark1104): either the [tools.toolObjs](#_bookmark1121) array or [tools.activeTool](#_bookmark1107).

#### Method summary

The following methods are available for the ToolObj object.
***Note:** The following methods are used only when creating extensible tools.*

| **Method**                                       | **Description**                                                                                                                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toolObj.enablePIControl()](#_bookmark1092)      | Enables or disables the specified control in a Property inspector. Used only when creating extensible tools.                                                                    |
| [toolObj.setIcon()](#_bookmark1095)              | Identifies a PNG file to use as a tool icon in the Flash Tools panel.                                                                                                           |
| [toolObj.setMenuString()](#_bookmark1096)        | Sets the string that appears in the pop-up menu as the name for the tool.                                                                                                       |
| [toolObj.setOptionsFile()](#_bookmark1097)       | Associates an XML file with the tool.                                                                                                                                           |
| [toolObj.setPI()](#_bookmark1098)                | Sets a particular Property inspector to be used when the tool is activated.                                                                                                     |
| [toolObj.setToolName()](#_bookmark1099)          | Assigns a name to the tool for the configuration of the Tools panel.                                                                                                            |
| [toolObj.setToolTip()](#_bookmark1100)           | Sets the tooltip that appears when the mouse is held over the tool icon.                                                                                                        |
| [toolObj.showPIControl()](#_bookmark1101)        | Shows or hides a control in the Property inspector.                                                                                                                             |
| [toolObj.showTransformHandles()](#_bookmark1102) | Called in the [configureTool()](#_bookmark18) method of an extensible tool’s JavaScript file to indicate that the free transform handles should appear when the tool is active. |

#### Property summary

The following properties are available for the ToolObj object:

| **Property**                       | **Description**                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------|
| [toolObj.depth](#toolObj.depth)    | An integer that specifies the depth of the tool in the pop-up menu in the Tools panel. |
| [toolObj.iconID](#_bookmark1093)   | An integer that specifies the resource ID of the tool.                                 |
| [toolObj.position](#_bookmark1094) | Read-only; an integer specifying the position of the tool in the Tools panel.          |

<span id="toolObj.depth" class="anchor"></span>

