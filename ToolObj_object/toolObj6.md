## toolObj.setOptionsFile()

#### Availability

Flash MX 2004.

#### Usage

toolObj.setOptionsFile(xmlFile)

#### Parameters

**xmlFile** A string that specifies the name of the XML file that has the description of the tool’s options. The XML file must be placed in the same folder as the JSFL file.

#### Returns

Nothing.

#### Description

Method; associates an XML file with the tool. The file specifies the options to appear in a modal panel that is invoked by an Options button in the Property inspector. You would usually use this method in the configureTool() function inside your JSFL file. See [configureTool()](#!AdobeDocs/developers-animatesdk-docs/master/Top-Level_Functions_and_Methods/configureTool.md).
For example, the PolyStar.xml file specifies three options associated with the Polygon tool:
\<properties\>
\<property name="Style" variable="style" list="polygon,star" defaultValue="0" type="Strings"/\>
\<property name="Number of Sides" variable="nsides"
min="3" max="32"
defaultValue="5" type="Number" /\>
\<property name="Star point size" variable="pointParam" min="0"
max="1" defaultValue=".5" type="Double" /\>
\</properties\>

#### Example

```javascript
The following example specifies that the file named PolyStar.xml is associated with the currently active tool. This code is taken from the sample PolyStar.jsfl file (see ["Sample PolyStar tool" on page 17](#_bookmark10)):
theTool = fl.tools.activeTool; theTool.setOptionsFile("PolyStar.xml");

```