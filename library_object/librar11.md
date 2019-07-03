## library.moveToFolder()

#### Availability

Flash MX 2004.

#### Usage

library.moveToFolder(folderPath \[, itemToMove \[, bReplace\]\])

#### Parameters

**folderPath** A string that specifies the path to the folder in the form "FolderName" or "FolderName/FolderName". To move an item to the top level, specify an empty string ("") for *folderPath*.
**itemToMove** A string that specifies the name of the item to move. If *itemToMove* is not specified, the currently selected items move. This parameter is optional.
**bReplace** A Boolean value. If an item with the same name already exists, specifying true for the *bReplace* parameter replaces the existing item with the item being moved. If false, the name of the dropped item changes to a unique name. The default value is false. This parameter is optional.

#### Returns

A Boolean value: true if the item moves successfully; false otherwise.

#### Description

Method; moves the currently selected or specified library item to a specified folder. If the *folderPath* parameter is empty, the items move to the top level.

#### Example

```
The following example moves the item Symbol\_1 to the library folder new and replaces the item in that folder with the same name:
fl.getDocumentDOM().library.moveToFolder("new", "Symbol\_1", true);

```