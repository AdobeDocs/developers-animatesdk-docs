## soundItem.lastModifiedDate

#### Availability

Flash Pro CS6.

#### Usage

soundItem.lastModifiedDate

#### Description

Read-only property; a hexadecimal value indicating the modification date and time of the sound item. This value is incremented every time the sound item is imported. For example, selecting the Update button from the Sound Properties dialog will trigger an import.

#### Example

```javascript
Assuming the first item in the Library is a sound item, the following code displays a hex number as described above.
var libItem = fl.getDocumentDOM().library.items\[0\];
fl.trace("Mod date when imported = " + libItem.lastModifiedDate);

```