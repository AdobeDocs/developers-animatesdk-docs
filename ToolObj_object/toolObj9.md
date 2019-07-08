## toolObj.setToolTip()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setToolTip(toolTip)

#### Parameters

**toolTip** A string that specifies the tooltip to use for the tool.

#### Returns

Nothing.

#### Description

Method; sets the tooltip that appears when the mouse is held over the tool icon. This method is used only when you create extensible tools.

#### Example

```javascript
The following example specifies that the tooltip for the tool should be PolyStar Tool. This code is taken from the sample PolyStar.jsfl file (se[e "Sample PolyStar tool" on page 17](#_bookmark10)):
theTool = fl.tools.activeTool; theTool.setToolTip("PolyStar Tool");

```