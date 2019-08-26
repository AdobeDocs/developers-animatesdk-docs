## soundItem.fileLastModifiedDate

#### Availability

Flash CS4 Professional.

#### Usage

soundItem.fileLastModifiedDate

#### Description

Read-only property: a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. If the file no longer exists, this value is "00000000".

#### Example

```javascript
Assuming that the first item in the Library is a sound item, the following code displays a hexadecimal number as described above.
var libItem = fl.getDocumentDOM().library.items\[0\];
fl.trace("Mod date when imported = " + libItem.fileLastModifiedDate);

```
#### See also

[soundItem.sourceFileExists](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt10.md), [soundItem.sourceFileIsCurrent](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt11.md), [soundItem.sourceFilePath](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt12.md), [FLfile.getModificationDate()](#!AdobeDocs/developers-animatesdk-docs/test/FLfile_object/FLfile6.md)
