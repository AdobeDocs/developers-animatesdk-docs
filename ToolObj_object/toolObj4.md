## toolObj.setIcon()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setIcon(file)

#### Parameters

**file** A string that specifies the name of the PNG file to use as the icon. The PNG file must be placed in the same folder as the JSFL file.

#### Returns

Nothing.

#### Description

Method; identifies a PNG file to use as a tool icon in the Tools panel. This method is used only when you create extensible tools.

#### Example

```
The following example specifies that the image in the PolyStar.png file should be used as the icon for the tool named
PolyStar. This code is taken from the sample PolyStar.jsfl file (see [“Sample PolyStar tool” on page 17](#_bookmark10)):
theTool = fl.tools.activeTool; theTool.setIcon("PolyStar.png");

```