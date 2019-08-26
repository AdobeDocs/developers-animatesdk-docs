## FLfile.platformPathToURI()

#### Availability

Flash CS4 Professional.

#### Usage

FLfile.platformPathToURI(fileName)

#### Parameters

**fileName** A string, expressed in a platform-specific format, specifying the filename you want to convert.

#### Returns

A string expressed as a file:/// URI.

#### Description

Method; converts a filename in a platform-specific format to a file:/// URI.

#### Example

```javascript
The following example converts a filename from a platform-specific format to a file:/// URI, which is passed to
outputPanel.save():
var myFilename = "C:\\\\outputPanel.txt";
var myURI=FLfile.platformPathToURI(myFilename); fl.outputPanel.save(myURI);

```
#### See also

[FLfile.uriToPlatformPath()](#!AdobeDocs/developers-animatesdk-docs/test/FLfile_object/FLfile14.md)
