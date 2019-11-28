## toolObj summary

#### Availability

Flash MX 2004.

#### Description

A ToolObj object represents an individual tool in the Tools panel. To access a ToolObj object, use properties of the [Tools object](../Tools_object/tools_summary.md): either the [tools.toolObjs](../Tools_object/tools11.md) array or [tools.activeTool](../Tools_object/tools.md).

#### Method summary

The following methods are available for the ToolObj object.

***Note:** The following methods are used only when creating extensible tools.*

| **Method**                                       | **Description**                                                                                                                                                                 |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [toolObj.enablePIControl()](../ToolObj_object/toolObj1.md)      | Enables or disables the specified control in a Property inspector. Used only when creating extensible tools.                                                                    |
| [toolObj.setIcon()](../ToolObj_object/toolObj4.md)              | Identifies a PNG file to use as a tool icon in the Flash Tools panel.                                                                                                           |
| [toolObj.setMenuString()](../ToolObj_object/toolObj5.md)        | Sets the string that appears in the pop-up menu as the name for the tool.                                                                                                       |
| [toolObj.setOptionsFile()](../ToolObj_object/toolObj6.md)       | Associates an XML file with the tool.                                                                                                                                           |
| [toolObj.setPI()](../ToolObj_object/toolObj7.md)                | Sets a particular Property inspector to be used when the tool is activated.                                                                                                     |
| [toolObj.setToolName()](../ToolObj_object/toolObj8.md)          | Assigns a name to the tool for the configuration of the Tools panel.                                                                                                            |
| [toolObj.setToolTip()](../ToolObj_object/toolObj9.md)           | Sets the tooltip that appears when the mouse is held over the tool icon.                                                                                                        |
| [toolObj.showPIControl()](../ToolObj_object/toolOb10.md)        | Shows or hides a control in the Property inspector.                                                                                                                             |
| [toolObj.showTransformHandles()](../ToolObj_object/toolOb11.md) | Called in the [configureTool()](../Top-Level_Functions_and_Methods/configureTool.md) method of an extensible tool’s JavaScript file to indicate that the free transform handles should appear when the tool is active. |

#### Property summary

The following properties are available for the ToolObj object:

| **Property**                       | **Description**                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------|
| [toolObj.depth](../ToolObj_object/toolObj.md)    | An integer that specifies the depth of the tool in the pop-up menu in the Tools panel. |
| [toolObj.iconID](../ToolObj_object/toolObj2.md)   | An integer that specifies the resource ID of the tool.                                 |
| [toolObj.position](../ToolObj_object/toolObj3.md) | Read-only; an integer specifying the position of the tool in the Tools panel.          |

<span id="toolObj.depth" class="anchor"></span>

