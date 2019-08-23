## toolObj.iconID

#### Availability

Flash MX 2004.

#### Usage

toolObj.iconID

#### Description

Read-only property; an integer with a value of -1. This property is used only when you create extensible tools. An iconID value of -1 means that Flash will not try find an icon for the tool. Instead, the script for the tool should specify the icon to display in the Tools panel; see [toolObj.setIcon()](#!AdobeDocs/developers-animatesdk-docs/test/ToolObj_object/toolObj4.md).

#### Example

```javascript
The following example assigns a value of -1 (the icon ID of the current tool) to the toolIconID variable:
var toolIconID = fl.tools.activeTool.iconID

```