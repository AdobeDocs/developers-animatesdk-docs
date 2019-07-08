## FLfile.getAttributes()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.getAttributes(fileOrFolderURI)

#### Parameters

**fileOrFolderURI** A string, expressed as a file:/// URI, specifying the file or folder whose attributes you want to retrieve.

#### Returns

A string that represents the attributes of the specified file or folder.
Results are unpredictable if the file or folder doesn’t exist. You should use [FLfile.exists()](#_bookmark563) before using this method.

#### Description

Method; returns a string representing the attributes of the specified file or folder, or an empty string if the file has no specific attributes (that it, it is not read-only, not hidden, and so on). You should always use [FLfile.exists()](#_bookmark563) to test for the existence of a file or folder before using this method.
Characters in the string represent the attributes as follows:

-   R — *fileOrFolderURI* is read-only

-   D — *fileOrFolderURI* is a folder (directory)

-   H — *fileOrFolderURI* is hidden (Windows only)

-   S — *fileOrFolderURI* is a system file or folder (Windows only)

-   A — *fileOrFolderURI* is ready for archiving (Windows only)

For example, if *fileOrFolderURI* is a hidden folder, the string returned is "DH".

#### Example

```javascript
The following example gets the attributes of the file mydata.txt and displays an alert box if the file is read-only.
var URI = "file:///c\|/temp/mydata.txt"; if (FLfile.exists(URI)){
var attr = FLfile.getAttributes(URI);
if (attr && (attr.indexOf("R") != -1)) { // Returned string contains R. alert(URI + " is read only!");
}
}

```
#### See also

[FLfile.setAttributes()](#_bookmark575)
