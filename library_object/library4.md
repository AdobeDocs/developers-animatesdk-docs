## library.editItem()

#### Availability

Flash MX 2004.

#### Usage

*library.editItem([namePath])*

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, you can specify its name and path using slash notation. If *namePath* is not specified, the single selected library item opens in Edit mode. If none or more than one item in the library is currently selected, the first scene in the main timeline appears for editing. This parameter is optional.

#### Returns

A Boolean value: *true* if the specified item exists and can be edited; *false* otherwise.

#### Description

Method; opens the currently selected or specified item in Edit mode.

#### Example

```javascript
The following example opens the item circle in the test folder of the library for editing:

fl.getDocumentDOM().library.editItem("test/circle");

```