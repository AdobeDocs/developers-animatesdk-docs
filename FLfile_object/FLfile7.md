## FLfile.getModificationDateObj()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.getModificationDateObj(fileOrFolderURI)

#### Parameters

**fileOrFolderURI** A string, expressed as a file:/// URI, specifying the file or folder whose modification date and time you want to retrieve as a JavaScript Date object.

#### Returns

A JavaScript Date object that represents the date and time when the specified file or folder was last modified. If the file or folder doesn’t exist, the object contains information indicating that the file or folder was created at midnight GMT on December 31, 1969.

#### Description

Method; returns a JavaScript Date object that represents the date and time when the specified file or folder was last modified.

#### Example

```javascript
The following example displays (in human-readable form) the date a file was last modified, in the Output panel:
// Make sure the specified file exists.
var file1Date = FLfile.getModificationDateObj("file:///c\|/temp/file1.txt"); trace(file1Date);

```
#### See also

[FLfile.getCreationDateObj()](../FLfile_object/FLfile5.md), [FLfile.getModificationDate()](../FLfile_object/FLfile6.md)
