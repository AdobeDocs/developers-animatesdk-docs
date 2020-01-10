## library.selectItem()

#### Availability

Flash MX 2004.

#### Usage

*library.selectItem(namePath [, bReplaceCurrentSelection [, bSelect]])*

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, you can specify its name and path using slash notation.

**bReplaceCurrentSelection** A Boolean value that specifies whether to replace the current selection or add the item to the current selection. The default value is true (replace current selection). This parameter is optional.

**bSelect** A Boolean value that specifies whether to select or deselect an item. The default value is *true* (select). This parameter is optional.

#### Returns

A Boolean value: *true* if the specified item exists; false otherwise.

#### Description

Method; selects a specified library item.

#### Example

```javascript
The following example changes the current selection in the library to Symbol_1 inside untitled Folder_1:

fl.getDocumentDOM().library.selectItem("untitled Folder_1/Symbol_1");

The following example extends what is currently selected in the library to include Symbol_1 inside untitled Folder_1:

fl.getDocumentDOM().library.selectItem("untitled Folder_1/Symbol_1", false);

The following example deselects Symbol_1 inside untitled Folder_1 and does not change other selected items:

fl.getDocumentDOM().library.selectItem("untitled Folder_1/Symbol_1", true, false);

```