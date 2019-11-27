## library.newFolder()

#### Availability

Flash MX 2004.

#### Usage

*library.newFolder([folderPath])*

#### Parameters

**folderPath** A string that specifies the name of the folder to be created. If it is specified as a path, and the path doesn’t exist, the path is created. This parameter is optional.

#### Returns

A Boolean value: true if folder is created successfully; *false* otherwise.

#### Description

Method; creates a new folder with the specified name, or a default name (*"untitled folder \#"*) if no *folderName*
parameter is provided, in the currently selected folder.

#### Example

```javascript
The following example creates two new library folders. The second folder is a subfolder of the first folder:

fl.getDocumentDOM().library.newFolder("first/second");

```