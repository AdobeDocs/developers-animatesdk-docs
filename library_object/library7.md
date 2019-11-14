## library.getItemType()

#### Availability

Flash MX 2004.

#### Usage

library.getItemType(\[namePath\])

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, specify its name and path using slash notation. If *namePath* is not specified, Flash provides the type of the current selection. If more than one item is currently selected and no *namePath* is provided, Flash ignores the command. This parameter is optional.

#### Returns

A string value specifying the type of object. For possible return values, see [item.itemType](../Item_object/item4.md).

#### Description

Method; gets the type of object currently selected or specified by a library path.

#### Example

```javascript
The following example shows a dialog box that contains the item type of Symbol\_1 located in the Folder\_1/Folder\_2
folder:
alert(fl.getDocumentDOM().library.getItemType("Folder\_1/Folder\_2/Symbol\_1"));

```