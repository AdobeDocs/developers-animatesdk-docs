## document.libraryPath

#### Availability

Flash CS4 Professional.

#### Usage

document.libraryPath

#### Description

Property; a string that contains a list of items in the document’s ActionScript 3.0 Library path, which specifies the location of SWC files or folders containing SWC files. Items in the string are delimited by semi-colons. In the authoring tool, the items are specified by choosing File \Publish Settings and then choosing ActionScript 3.0 Script Settings on the Flash tab.

#### Example

```javascript
The following adds the ../Files folder to the document’s Library path and then displays the path Library path in the Output panel:
var myDoc = fl.getDocumentDOM() fl.trace(myDoc.libraryPath);
myDoc.libraryPath = "../Files;" + myDoc.libraryPath; fl.trace(myDoc.libraryPath);

```
#### See also

[document.externalLibraryPath](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume69.md),[document.sourcePath](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum36.md), [fl.libraryPath](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl39.md)/fl39.md)
