## toolObj.setPI()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setPI(pi)

#### Parameters

**pi** A string that specifies the Property inspector to invoke for this tool.

#### Returns

Nothing.

#### Description

Method; specifies which Property inspector should be used when the tool is activated. This method is used only when you create extensible tools. Acceptable values are "shape" (the default), "text", and "movie".

#### Example

```
The following example specifies that the shape Property inspector should be used when the tool is activated. This code is taken from the sample PolyStar.jsfl file (see ["Sample PolyStar tool" on page 17](#_bookmark10)):
theTool = fl.tools.activeTool; theTool.setPI("shape");

```