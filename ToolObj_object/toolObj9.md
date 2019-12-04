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

The following example specifies that the tooltip for the tool should be PolyStar Tool. This code is taken from the sample PolyStar.jsfl file (see[ "Sample PolyStar tool"](../Introduction/Sample_implementations.md#Sample-PolyStar-tool)):

```javascript
theTool = fl.tools.activeTool;
theTool.setToolTip("PolyStar Tool");

```