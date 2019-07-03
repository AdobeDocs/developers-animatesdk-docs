## bitmapItem.lastModifiedDate

#### Availability

Flash Pro CS6.

#### Usage

bitmapItem.lastModifiedDate

#### Description

Read-only property; a hexadecimal value indicating the modification date and time of the bitmap item. This value is incremented every time the bitmap item is imported. For example, selecting the Update button from the Bitmap Properties dialog will trigger an import.

#### Example

```
Assuming the first item in the Library is a bitmap item, the following code displays a hex number as described above.
var libItem = fl.getDocumentDOM().library.items\[0\];
fl.trace("Mod date when imported = " + libItem.lastModifiedDate);

```
#### See also

[bitmapItem.sourceFileExists](#_bookmark60), [bitmapItem.sourceFileIsCurrent](#_bookmark61), [bitmapItem.sourceFilePath](#_bookmark62), [FLfile.getModificationDate()](#_bookmark568)
