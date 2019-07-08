## document.exportPublishProfile()

#### Availability

Flash MX 2004.

#### Usage

document.exportPublishProfile(fileURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the path of the XML file to which the profile is exported.

#### Returns

Nothing.

#### Description

Method; exports the currently active profile to an XML file.

#### Example

```javascript
The following example exports the currently active profile to the file named profile.xml in the folder /Documents and Settings/username/Desktop on the C drive:
fl.getDocumentDOM().exportPublishProfile('file:///C\|/Documents and Settings/username/Desktop/profile.xml');

```
#### See also

[document.exportPublishProfileString()](#document.exportPublishProfileString()), [document.importPublishProfile()](#_bookmark226)

<span id="document.exportPublishProfileString()" class="anchor"></span>
