## library summary

#### Availability

Flash MX 2004.

#### Description

The library object represents the Library panel. It is a property of the Document object (see [document.library](../Document_object/docume98.md)) and can be accessed by *fl.getDocumentDOM().library*.

The library object contains an array of items of different types, including symbols, bitmaps, sounds, and video.

#### Method summary

The following methods are available for the library object:

| **Method**                                                  | **Description**                                                                                                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [library.addItemToDocument()](../library_object/library.md) | Adds the current or specified item to the Stage at the specified position.                                                                                       |
| [library.addNewItem()](../library_object/library1.md)                       | Creates a new item of the specified type in the Library panel and sets the new item to the currently selected item.                                              |
| [library.deleteItem()](../library_object/library2.md)                       | Deletes the current items or a specified item from the Library panel.                                                                                            |
| [library.duplicateItem()](../library_object/library3.md)                    | Makes a copy of the currently selected or specified item.                                                                                                        |
| [library.editItem()](../library_object/library4.md)                         | Opens the currently selected or specified item in Edit mode.                                                                                                     |
| [library.findItemIndex()](../library_object/library5.md)                    | Returns the library item’s index value (zero-based).                                                                                                             |
| [library.getItemProperty()](../library_object/library6.md)                  | Gets the property for the selected item.                                                                                                                         |
| [library.getItemType()](../library_object/library7.md)                      | Gets the type of object currently selected or specified by a library path.                                                                                       |
| [library.getSelectedItems()](../library_object/library8.md)                 | Gets the array of all currently selected items in the library.                                                                                                   |
| [library.itemExists()](../library_object/library9.md)                       | Checks to see if a specified item exists in the library.                                                                                                         |
| [library.moveToFolder()](../library_object/librar11.md)                     | Moves the currently selected or specified library item to a specified folder.                                                                                    |
| [library.newFolder()](../library_object/librar12.md)                        | Creates a new folder with the specified name, or a default name (*"untitled folder \#"*) if no folderName parameter is provided, in the currently selected folder. |
| [library.renameItem()](../library_object/librar13.md)                       | Renames the currently selected library item in the Library panel.                                                                                                |
| [library.selectAll()](../library_object/librar14.md)                        | Selects or deselects all items in the library.                                                                                                                   |
| [library.selectItem()](../library_object/librar15.md)                       | Selects a specified library item.                                                                                                                                |
| [library.selectNone()](../library_object/librar16.md)                       | Deselects all the library items.                                                                                                                                 |
| [library.setItemProperty()](../library_object/librar17.md)                  | Sets the property for all selected library items (ignoring folders).                                                                                             |
| [library.updateItem()](../library_object/librar19.md)                       | Updates the specified item.                                                                                                                                      |

#### Property summary for the library object

The following property is available for the library object:

| **Property**                         | **Description**                                              |
|--------------------------------------|--------------------------------------------------------------|
| [library.items](../library_object/librar10.md)       | An array of Item objects in the library                      |
| [library.unusedItems](../library_object/librar18.md) | An array of library Items that are not used in the document. |

<span id="library.addItemToDocument()" class="anchor"></span>

