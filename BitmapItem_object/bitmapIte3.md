## bitmapItem.fileLastModifiedDate

#### Availability

Flash CS4 Professional.

#### Usage

bitmapItem.fileLastModifiedDate

#### Description

Read-only property; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970 and the modification date of the original file at the time the file was imported to the library. If the file no longer exists, this value is "00000000".

#### Example

```javascript
Assuming the first item in the Library is a bitmap item, the following code displays a hex number as described above.
var libItem = fl.getDocumentDOM().library.items\[0\];
fl.trace("Mod date when imported = " + libItem.fileLastModifiedDate);

```
#### See also

[bitmapItem.sourceFileExists](#_bookmark60), [bitmapItem.sourceFileIsCurrent](#_bookmark61), [bitmapItem.sourceFilePath](#_bookmark62), [FLfile.getModificationDate()](#_bookmark568)
