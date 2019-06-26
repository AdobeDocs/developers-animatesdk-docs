## FLfile.remove()

#### Availability

> Flash MX 2004 7.2.

#### Usage

> FLfile.remove(fileOrFolderURI)

#### Parameters

> **fileOrFolderURI** A string, expressed as a file:/// URI, specifying the file or folder you want to remove (delete).

#### Returns

> A Boolean value of true if successful; false otherwise.

#### Description

> Method; deletes the specified file or folder. If the folder contains files, those files will be deleted as well. Files with the R (read-only) attribute cannot be removed.

#### Examples

> The following example warns a user if a file exists and then deletes it if the user chooses to do so:
>
> var fileURI = prompt ("Enter file/folder to be deleted: ", "file:///c\|/temp/delete.txt"); if (FLfile.exists(fileURI)) {
>
> var confirm = prompt("File exists. Delete it? (y/n)", "y"); if (confirm == "y" \|\| confirm == "Y") {
>
> if(FLfile.remove(fileURI)) { alert(fileURI + " is deleted.");
>
> }
>
> else {
>
> alert("fail to delete " + fileURI);
>
> }
>
> }
>
> }
>
> else {
>
> alert(fileURI + " does not exist");
>
> }
>
> The following example deletes a configuration file created by an application:
>
> if(FLfile.remove("file:///C\|/MyApplication/config.ini")) { alert("Configuration file deleted");
>
> }
>
> The following example deletes the Configuration folder and its contents:
>
> FLfile.remove("file:///C\|/MyApplication/Configuration/");

#### See also

> [FLfile.createFolder()](#_bookmark562), [FLfile.getAttributes()](#_bookmark564)
