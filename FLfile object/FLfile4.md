## FLfile.getCreationDate()

#### Availability

> Flash MX 2004 7.2.

#### Usage

> FLfile.getCreationDate(fileOrFolderURI)

#### Parameters

> **fileOrFolderURI** A string, expressed as a file:/// URI, specifying the file or folder whose creation date and time you want to retrieve as a hexadecimal string.

#### Returns

> A string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970 and the time the file or folder was created, or "00000000" if the file or folder doesn’t exist.

#### Description

> Method; specifies how many seconds have passed between January 1, 1970 and the time the file or folder was created. This method is used primarily to compare the creation or modification dates of files or folders.

#### Example

> The following example determines whether a file has been modified since it was created:
>
> // Make sure the specified file exists
>
> var fileURI = "file:///C\|/MyApplication/MyApp.fla"; var creationTime = FLfile.getCreationDate(fileURI);
>
> var modificationTime = FLfile.getModificationDate(fileURI); if ( modificationTime \> creationTime ) {
>
> alert("The file has been modified since it was created.");
>
> }
>
> else {
>
> alert("The file has not been modified since it was created.");
>
> }

#### See also

> [FLfile.getCreationDateObj()](#FLfile.getCreationDateObj()), [FLfile.getModificationDate()](#_bookmark567)

<span id="FLfile.getCreationDateObj()" class="anchor"></span>
