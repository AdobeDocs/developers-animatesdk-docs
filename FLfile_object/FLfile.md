## FLfile.copy()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.copy(fileURI, copyURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the file you want to copy.
**copyURI** A string, expressed as a file:/// URI, that specifies the location and name of the copied file.

#### Returns

A Boolean value of true if successful; false otherwise.

#### Description

Method; copies a file from one location to another. This method returns false if *copyURI* already exists.

#### Example

```javascript
The following example makes a backup copy of a configuration file named config.ini and places it inside the same folder in which it is located, with a new name:
var originalFileURI="file:///C\|/Program Files/MyApp/config.ini"; var newFileURI="file:///C\|/Program Files/MyApp/config\_backup.ini"; FLfile.copy(originalFileURI, newFileURI);
If you prefer, you can perform the same task with a single command:
FLfile.copy("file:///C\|:/Program Files/MyApp/config.ini", "file:///C\|/Program Files/MyApp/config\_backup.ini");

```