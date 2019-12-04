## toolObj.setToolName()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setToolName(name)

#### Parameters

**name** A string that specifies the name of the tool.

#### Returns

Nothing.

#### Description

Method; assigns a name to the tool for the configuration of the Tools panel. This method is used only when you create extensible tools. The name is used only by the XML layout file that Flash reads to construct the Tools panel. The name does not appear in the Flash user interface.

#### Example

The following example assigns the name polystar to the tool named theTool. This code is taken from the sample PolyStar.jsfl file (see[ "Sample PolyStar tool"](../Introduction/Sample_implementations.md#Sample-PolyStar-tool)):

```javascript
theTool = fl.tools.activeTool;
theTool.setToolName("polystar");

```