## videoItem.exportToFLV()

#### Availability

Flash CS4 Professional.

#### Usage

videoItem.exportToFLV(fileURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the path and name of the exported file.

#### Returns

A Boolean value of true if the file is exported successfully; false otherwise.

#### Description

Method; exports the specified item to an FLV file.

#### Example

```
Assuming that the first item in the Library is a video item, the following code exports it as an FLV file:
var videoFileURL = "file:///C\|/out.flv";
var libItem = fl.getDocumentDOM().library.items\[0\]; libItem.exportToFLV(videoFileURL);

```