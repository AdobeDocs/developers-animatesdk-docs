## library.itemExists()

#### Availability

Flash MX 2004.

#### Usage

library.itemExists(namePath)

#### Parameters

**namePath** A string that specifies the name of the item. If the item is in a folder, specify its name and path using slash notation.

#### Returns

A Boolean value: true if the specified item exists in the library; false otherwise.

#### Description

Method; checks to see if a specified item exists in the library.

#### Example

```javascript
The following example displays true or false in a dialog box, depending on whether the item Symbol\_1 exists in the
Folder\_1 library folder:
alert(fl.getDocumentDOM().library.itemExists('Folder\_1/Symbol\_1'));

```