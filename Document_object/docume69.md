## document.externalLibraryPath

#### Availability

Flash CS4 Professional.

#### Usage

document.externalLibraryPath

#### Description

Property; a string that contains a list of items in the document’s ActionScript 3.0 External library path, which specifies the location of SWC files used as runtime shared libraries. Items in the string are delimited by semi-colons. In the authoring tool, the items are specified by choosing File \Publish Settings and then choosing ActionScript 3.0 Script Settings on the Flash tab.

#### Example

```
The following example sets the document’s External library path to "." and "../mySWCLibrary":
var myDocument = fl.getDocumentDOM(); myDocument.externalLibraryPath = ".;../mySWCLibrary"; fl.trace(myDocument.externalLibraryPath);

```
#### See also

[document.libraryPath](#_bookmark233), [document.sourcePath](#_bookmark321),[fl.externalLibraryPath](#_bookmark480)
