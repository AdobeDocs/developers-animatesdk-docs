## library.addNewItem()

#### Availability

Flash MX 2004.

#### Usage

library.addNewItem(type \[, namePath\])

#### Parameters

**type** A string that specifies the type of item to create. The only acceptable values for *type* are "video", "movie clip", "button", "graphic", "bitmap", "screen", and "folder" (so, for example, you cannot add a sound to the library with this method). Specifying a folder path is the same as using [library.newFolder()](#_bookmark709) before calling this method.
>
**namePath** A string that specifies the name of the item to be added. If the item is in a folder, specify its name and path using slash notation. This parameter is optional.

#### Returns

A Boolean value: true if the item is successfully created; false otherwise.

#### Description

Method; creates a new item of the specified type in the Library panel and sets the new item to the currently selected item. For more information on importing items into the library, including items such as sounds, see [document.importFile()](#_bookmark225).

#### Example

```
The following example creates a new button item named start in a new folder named folderTwo: fl.getDocumentDOM().library.addNewItem("button", "folderTwo/start");

```