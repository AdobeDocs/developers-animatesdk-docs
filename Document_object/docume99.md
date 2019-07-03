## document.libraryPath

#### Availability

Flash CS4 Professional.

#### Usage

document.libraryPath

#### Description

Property; a string that contains a list of items in the document’s ActionScript 3.0 Library path, which specifies the location of SWC files or folders containing SWC files. Items in the string are delimited by semi-colons. In the authoring tool, the items are specified by choosing File \Publish Settings and then choosing ActionScript 3.0 Script Settings on the Flash tab.

#### Example

```
The following adds the ../Files folder to the document’s Library path and then displays the path Library path in the Output panel:
var myDoc = fl.getDocumentDOM() fl.trace(myDoc.libraryPath);
myDoc.libraryPath = "../Files;" + myDoc.libraryPath; fl.trace(myDoc.libraryPath);

```
#### See also

[document.externalLibraryPath](#_bookmark194),[document.sourcePath](#_bookmark321), [fl.libraryPath](#_bookmark501)
