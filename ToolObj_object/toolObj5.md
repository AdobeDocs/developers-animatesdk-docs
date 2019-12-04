## toolObj.setMenuString()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setMenuString(menuStr)

#### Parameters

**menuStr** A string that specifies the name that appears in the pop-up menu as the name for the tool.

#### Returns

Nothing.

#### Description

Method; sets the string that appears in the pop-up menu as the name for the tool. This method is used only when you create extensible tools.

#### Example

The following example specifies that the tool named theTool should display the name "PolyStar Tool" in its pop-up menu. This code is taken from the sample PolyStar.jsfl file (see ["Sample PolyStar tool"](../Introduction/Sample_implementations.md#Sample-PolyStar-tool)):

```javascript
theTool = fl.tools.activeTool;
theTool.setMenuString("PolyStar Tool");

```