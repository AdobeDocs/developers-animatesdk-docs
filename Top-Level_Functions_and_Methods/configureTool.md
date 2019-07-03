## configureTool()

#### Availability

Flash MX 2004.

#### Usage

function configureTool() {
>
// statements
>
}

#### Parameters

None.

#### Returns

Nothing.

#### Description

Function; called when Flash opens and the extensible tool is loaded into the Tools panel. Use this function to set any information Flash needs to know about the tool.

#### Example

```
The following examples show two possible implementations of this function:
function configureTool() { theTool = fl.tools.activeTool; theTool.setToolName("myTool"); theTool.setIcon("myTool.png");
theTool.setMenuString("My Tool's menu string"); theTool.setToolTip("my tool's tool tip"); theTool.setOptionsFile( "mtTool.xml" );
}
function configureTool() { theTool = fl.tools.activeTool;
theTool.setToolName("ellipse"); theTool.setIcon("Ellipse.png"); theTool.setMenuString("Ellipse"); theTool.setToolTip("Ellipse"); theTool.showTransformHandles( true );
}

```