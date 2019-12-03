## videoItem.lastModifiedDate

#### Availability

Flash Pro CS6.

#### Usage

*videoItem.lastModifiedDate*

#### Description

Read-only property; a hexadecimal value indicating the modification date and time of the video item. This value is incremented every time the video item is imported.

#### Example

Assuming the first item in the Library is a video item, the following code displays a hex number as described above.

```javascript
var libItem = fl.getDocumentDOM().library.items[0];
fl.trace("Mod date when imported = " + libItem.lastModifiedDate);

```