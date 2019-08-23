## FLfile.uriToPlatformPath()

#### Availability

Flash CS4 Professional.

#### Usage

FLfile.uriToPlatformPath(fileURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, specifying the filename you want to convert.

#### Returns

A string representing a platform-specific path.

#### Description

Method; converts a filename expressed as a file:/// URI to a platform-specific format.

#### Example

```javascript
The following example converts a file:/// URI to a platform-specific format:
var dir =(fl.configDirectory);
var URI = FLfile.platformPathToURI(dir); fl.trace(URI == fl.configURI); // displays "true"

```
#### See also

[FLfile.platformPathToURI()](#!AdobeDocs/developers-animatesdk-docs/test/FLfile_object/FLfile10.md)
