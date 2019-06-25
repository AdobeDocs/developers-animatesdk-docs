## document.importPublishProfileString()

#### Availability

> Flash CS4 Professional.

#### Usage

> document.importPublishProfileString(xmlString)

#### Parameters

> **xmlString** A string that contains the XML data to be imported as the current profile.

#### Returns

> A Boolean value of true if the string was successfully imported; false otherwise.

#### Description

> Method: imports an XML string that represents a publish profile and sets it as the current profile. To generate an XML string to import, use [document.exportPublishProfileString()](#_bookmark191) before using this method.

#### Example

> In the following example, the default profile is exported as an XML string. The standard JavaScript replace command is used to modify the XML string. The string is then imported, and the default ActionScript 3 output setting is set to ActionScript 1.
>
> var profileXML=fl.getDocumentDOM().exportPublishProfileString('Default'); fl.trace(profileXML);
>
> var newProfileXML = profileXML.replace("\<ActionScriptVersion\>3\</ActionScriptVersion\>", "\<ActionScriptVersion\>1\</ActionScriptVersion\>"); fl.getDocumentDOM().importPublishProfileString(newProfileXML);
