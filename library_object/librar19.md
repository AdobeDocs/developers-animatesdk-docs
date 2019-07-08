## library.updateItem()

#### Availability

Flash MX 2004.

#### Usage

library.updateItem(\[namePath\])

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, specify its name and path using slash notation. This is the same as right-clicking on an item and selecting Update from the menu in the user interface. If no name is provided, the current selection is updated. This parameter is optional.

#### Returns

A Boolean value: true if Flash updated the item successfully; false otherwise.

#### Description

Method; updates the specified item.

#### Example

```javascript
The following example displays a dialog box that shows whether the currently selected item is updated (true) or not (false):
alert(fl.getDocumentDOM().library.updateItem());

```