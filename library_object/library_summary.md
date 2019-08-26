## library summary

#### Availability

Flash MX 2004.

#### Description

The library object represents the Library panel. It is a property of the Document object (see [document.library](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume98.md)) and can be accessed by fl.getDocumentDOM().library.
The library object contains an array of items of different types, including symbols, bitmaps, sounds, and video.

#### Method summary

The following methods are available for the library object:

| **Method**                                                  | **Description**                                                                                                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [library.addItemToDocument()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library.md)) | Adds the current or specified item to the Stage at the specified position.                                                                                       |
| [library.addNewItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library1.md)                       | Creates a new item of the specified type in the Library panel and sets the new item to the currently selected item.                                              |
| [library.deleteItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library2.md)                       | Deletes the current items or a specified item from the Library panel.                                                                                            |
| [library.duplicateItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library3.md)                    | Makes a copy of the currently selected or specified item.                                                                                                        |
| [library.editItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library4.md)                         | Opens the currently selected or specified item in Edit mode.                                                                                                     |
| [library.findItemIndex()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library5.md)                    | Returns the library item’s index value (zero-based).                                                                                                             |
| [library.getItemProperty()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library6.md)                  | Gets the property for the selected item.                                                                                                                         |
| [library.getItemType()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library7.md)                      | Gets the type of object currently selected or specified by a library path.                                                                                       |
| [library.getSelectedItems()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library8.md)                 | Gets the array of all currently selected items in the library.                                                                                                   |
| [library.itemExists()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/library9.md)                       | Checks to see if a specified item exists in the library.                                                                                                         |
| [library.moveToFolder()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar11.md)                     | Moves the currently selected or specified library item to a specified folder.                                                                                    |
| [library.newFolder()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar12.md)                        | Creates a new folder with the specified name, or a default name ("untitled folder \#") if no folderName parameter is provided, in the currently selected folder. |
| [library.renameItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar13.md)                       | Renames the currently selected library item in the Library panel.                                                                                                |
| [library.selectAll()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar14.md)                        | Selects or deselects all items in the library.                                                                                                                   |
| [library.selectItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar15.md)                       | Selects a specified library item.                                                                                                                                |
| [library.selectNone()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar16.md)                       | Deselects all the library items.                                                                                                                                 |
| [library.setItemProperty()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar17.md)                  | Sets the property for all selected library items (ignoring folders).                                                                                             |
| [library.updateItem()](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar19.md)                       | Updates the specified item.                                                                                                                                      |

#### Property summary for the library object

The following property is available for the library object:

| **Property**                         | **Description**                                              |
|--------------------------------------|--------------------------------------------------------------|
| [library.items](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar10.md)       | An array of Item objects in the library                      |
| [library.unusedItems](#!AdobeDocs/developers-animatesdk-docs/test/library_object/librar18.md) | An array of library Items that are not used in the document. |

<span id="library.addItemToDocument()" class="anchor"></span>

