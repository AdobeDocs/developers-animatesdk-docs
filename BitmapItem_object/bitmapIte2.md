## bitmapItem.exportToFile()

#### Availability

Flash CS4 Professional.

#### Usage

bitmapItem.exportToFile(fileURI, quality)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the path and name of the exported file.
>
**quality** A number, from 1-100, that determines the quality of the exported image file. A higher number indicates higher quality. The default is 80. New in Flash CS6 Professional.

#### Returns

A Boolean value of true if the file was exported successfully; false otherwise.

#### Description

Method; exports the specified item to a PNG or JPG file.

#### Example

```
Assuming the first item in the Library is a bitmap item, the following code exports it as a JPG file:
var imageFileURL = "file:///C\|/exportTest/out.jpg"; var libItem = fl.getDocumentDOM().library.items\[0\]; libItem.exportToFile(imageFileURL);

```