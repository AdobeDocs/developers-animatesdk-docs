## FLfile.exists()

#### Availability

Flash MX 2004 7.2.

#### Usage

FLfile.exists(fileURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the file you want to verify.

#### Returns

A Boolean value of true if successful; false otherwise.

#### Description

Method; determines whether a specified file exists. If you specify a folder and a filename, the folder must already exist. To create folders, see [FLfile.createFolder()](#_bookmark562).

#### Examples

```
The following example checks for a file called mydata.txt in the temp folder and displays an alert box indicating whether the file exists:
var fileURI = "file:///c\|/temp/mydata.txt"; if (FLfile.exists(fileURI)) {
alert( fileURI + " exists.");
}
else {
alert( fileURI + " does not exist.");
}
The following example checks to see if a required configuration file exists in the MyApplication folder. If the file doesn’t exist, it is created.
var configFile = "file:///C\|/MyApplication/config.ini"; if (!FLfile.exists(configFile)) {
FLfile.write(configFile,"");
}

```
#### See also

[FLfile.write()](#_bookmark577)
