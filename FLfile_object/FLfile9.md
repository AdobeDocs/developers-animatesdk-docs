## FLfile.listFolder()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.listFolder(folderURI \[, filesOrDirectories\])

#### Parameters

**folderURI** A string, expressed as a file:/// URI, specifying the folder whose contents you want to retrieve. You can include a wildcard mask as part of *folderURI*. Valid wildcards are \* (matches one or more characters) and ? (matches a single character).
>
**filesOrDirectories** An optional string that specifies whether to return only filenames or only folder (directory) names. If omitted, both filenames and folder names are returned. Acceptable values are "files" and "directories".

#### Returns

An array of strings representing the contents of the folder. If the folder doesn’t exist or if no files or folders match the specified criteria, returns an empty array.

#### Description

Method; returns an array of strings representing the contents of the folder.

#### Examples

```
The following example returns three arrays. The first represents all the files in the C:\\temp folder, the second represents all the folders in the C:\\temp folder, and the third represents the files and folders in the C:\\temp folder:
var fileURI = "file:///C\|/temp/" ; var folderURI = "file:///C\|/temp" ;
var fileList1 = FLfile.listFolder(fileURI, "files"); // files
var fileList2 = FLfile.listFolder(folderURI, "directories"); //folders var fileList3 = FLfile.listFolder(folderURI); //files and folders fl.trace("Files: " + fileList1);
fl.trace("");
fl.trace("Folders: " + fileList2); fl.trace("");
fl.trace("Files and folders: " + fileList3);
The following example returns an array of all the text (.txt) files in the temp folder and displays the list in an alert box:
var folderURI = "file:///c\|/temp"; var fileMask = "\*.txt";
var list = FLfile.listFolder(folderURI + "/" + fileMask, "files"); if (list) {
alert(folderURI + " contains: " + list.join(" "));
}
The following example uses a file mask in the specified *folderURI* to return the names of all the executable files in the Windows application folder:
var executables = FLfile.listFolder("file:///C\|/WINDOWS/\*.exe","files"); alert(executables.join("\\n"));

```