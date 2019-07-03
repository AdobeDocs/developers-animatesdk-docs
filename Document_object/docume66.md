## document.exportPublishProfileString()

#### Availability

Flash CS4 Professional.

#### Usage

document.exportPublishProfileString( \[profileName\] )

#### Parameters

**profileName** A string that specifies the name of the profile to export to an XML string. This parameter is optional.

#### Returns

An XML string.

#### Description

Method: returns a string that specifies, in XML format, the specified profile. If you don’t pass a value for *profileName*, the current profile is exported.

#### Example

```
The following example stores an XML string that represents the current profile in a variable named profileXML and then displays it in the Output panel:
var profileXML=fl.getDocumentDOM().exportPublishProfileString(); fl.trace(profileXML);

```
#### See also

[document.exportPublishProfile()](#_bookmark190), [document.importPublishProfileString()](#_bookmark227)
