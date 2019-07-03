## library summary

#### Availability

Flash MX 2004.

#### Description

The library object represents the Library panel. It is a property of the Document object (see [document.library](#_bookmark232)) and can be accessed by fl.getDocumentDOM().library.
>
The library object contains an array of items of different types, including symbols, bitmaps, sounds, and video.

#### Method summary

The following methods are available for the library object:

| **Method**                                                  | **Description**                                                                                                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [library.addItemToDocument()](#library.addItemToDocument()) | Adds the current or specified item to the Stage at the specified position.                                                                                       |
| [library.addNewItem()](#_bookmark696)                       | Creates a new item of the specified type in the Library panel and sets the new item to the currently selected item.                                              |
| [library.deleteItem()](#_bookmark698)                       | Deletes the current items or a specified item from the Library panel.                                                                                            |
| [library.duplicateItem()](#_bookmark699)                    | Makes a copy of the currently selected or specified item.                                                                                                        |
| [library.editItem()](#_bookmark700)                         | Opens the currently selected or specified item in Edit mode.                                                                                                     |
| [library.findItemIndex()](#_bookmark701)                    | Returns the library item’s index value (zero-based).                                                                                                             |
| [library.getItemProperty()](#_bookmark702)                  | Gets the property for the selected item.                                                                                                                         |
| [library.getItemType()](#_bookmark703)                      | Gets the type of object currently selected or specified by a library path.                                                                                       |
| [library.getSelectedItems()](#_bookmark704)                 | Gets the array of all currently selected items in the library.                                                                                                   |
| [library.itemExists()](#_bookmark705)                       | Checks to see if a specified item exists in the library.                                                                                                         |
| [library.moveToFolder()](#_bookmark708)                     | Moves the currently selected or specified library item to a specified folder.                                                                                    |
| [library.newFolder()](#_bookmark709)                        | Creates a new folder with the specified name, or a default name ("untitled folder \#") if no folderName parameter is provided, in the currently selected folder. |
| [library.renameItem()](#_bookmark710)                       | Renames the currently selected library item in the Library panel.                                                                                                |
| [library.selectAll()](#_bookmark711)                        | Selects or deselects all items in the library.                                                                                                                   |
| [library.selectItem()](#_bookmark712)                       | Selects a specified library item.                                                                                                                                |
| [library.selectNone()](#_bookmark713)                       | Deselects all the library items.                                                                                                                                 |
| [library.setItemProperty()](#_bookmark714)                  | Sets the property for all selected library items (ignoring folders).                                                                                             |
| [library.updateItem()](#_bookmark716)                       | Updates the specified item.                                                                                                                                      |

#### Property summary for the library object

The following property is available for the library object:

| **Property**                         | **Description**                                              |
|--------------------------------------|--------------------------------------------------------------|
| [library.items](#_bookmark706)       | An array of Item objects in the library                      |
| [library.unusedItems](#_bookmark715) | An array of library Items that are not used in the document. |

<span id="library.addItemToDocument()" class="anchor"></span>

