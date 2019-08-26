## document.sourcePath

#### Availability

Flash CS4 Professional.

#### Usage

document.sourcePath

#### Description

Property; a string that contains a list of items in the document’s ActionScript 3.0 Source path, which specifies the location of ActionScript class files. Items in the string are delimited by semi-colons. In the authoring tool, the items are specified by choosing File \Publish Settings and then choosing ActionScript 3.0 Script Settings on the Flash tab.

#### Example

```javascript
The following example adds the ./Class files folder to the document’s Source path:
var myDoc = fl.getDocumentDOM(); fl.trace(myDoc.sourcePath);
myDoc.sourcePath = "./Class files;" + myDoc.sourcePath; fl.trace(myDoc.sourcePath);

```
#### See also

[document.externalLibraryPath](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume69.md), [document.libraryPath](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume99.md), [fl.sourcePath](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl72.md)/fl72.md)
