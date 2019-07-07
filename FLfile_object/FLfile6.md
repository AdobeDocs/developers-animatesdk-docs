## FLfile.getModificationDate()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.getModificationDate(fileOrFolderURI)

#### Parameters

**fileOrFolderURI** A string, expressed as a file:/// URI, specifying the file whose modification date and time you want to retrieve as a hexadecimal string.

#### Returns

A string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970 and the time the file or folder was last modified, or "00000000" if the file doesn’t exist.

#### Description

Method; specifies how many seconds have passed between January 1, 1970 and the time the file or folder was last modified. This method is used primarily to compare the creation or modification dates of files or folders.

#### Example

```
The following example compares the modification dates of two files and determines which of the two was modified more recently:
// Make sure the specified files exist.
file1 = "file:///C\|/MyApplication/MyApp.fla"; file2 = "file:///C\|/MyApplication/MyApp.as";
modificationTime1 = FLfile.getModificationDate(file1); modificationTime2 = FLfile.getModificationDate(file2) ; if(modificationTime1 \modificationTime2) {
alert("File 2 is older than File 1") ;
}
else if(modificationTime1 \< modificationTime2) { alert("File 1 is older than File 2") ;
}
else {
alert("File 1 and File 2 were saved at the same time") ;
}

```
#### See also

[FLfile.getCreationDate()](#_bookmark565), [FLfile.getModificationDateObj()](#FLfile.getModificationDateObj())

<span id="FLfile.getModificationDateObj()" class="anchor"></span>
