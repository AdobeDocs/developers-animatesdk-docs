## FLfile.createFolder()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.createFolder(folderURI)

#### Parameters

**folderURI** A folder URI that specifies the folder structure you want to create.

#### Returns

A Boolean value of true if successful; false if *folderURI* already exists.

#### Description

Method; creates one or more folders at the specified location.
You can create multiple folders at one time. For example, the following command creates both the MyData and the TempData folders if they don’t already exist:
FLfile.createFolder("file:///c\|/MyData/TempData")

#### Example

```javascript
The following example creates a folder and a subfolder under the configuration folder ([fl.configURI](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl13.md)/fl13.md)):
fl.trace(FLfile.createFolder(fl.configURI+"folder01/subfolder01"));
The following example attempts to create a folder called tempFolder at the root level on the C drive and displays an alert box indicating whether the operation was successful:
var folderURI = "file:///c\|/tempFolder"; if (FLfile.createFolder(folderURI)) {
alert("Created " + folderURI);
}
else {
alert(folderURI + " already exists");
}

```
#### See also

[FLfile.remove()](#!AdobeDocs/developers-animatesdk-docs/test/FLfile_object/FLfile12.md), [FLfile.write()](#!AdobeDocs/developers-animatesdk-docs/test/FLfile_object/FLfile15.md)
