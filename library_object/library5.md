## library.findItemIndex()

#### Availability

Flash MX 2004.

#### Usage

library.findItemIndex(namePath)

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, you can specify its name and path using slash notation.

#### Returns

An integer value representing the item’s zero-based index value.

#### Description

Method; returns the library item’s index value (zero-based). The library index is flat, so folders are considered part of the main index. Folder paths can be used to specify a nested item.

#### Example

```javascript
The following example stores the zero-based index value of the library item square, which is in the test folder, in the variable sqIndex, and then displays the index value in a dialog box:
var sqIndex = fl.getDocumentDOM().library.findItemIndex("test/square"); alert(sqIndex);

```