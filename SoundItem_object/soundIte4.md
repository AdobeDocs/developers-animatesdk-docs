## soundItem.exportToFile()

#### Availability

Flash CS4 Professional.

#### Usage

soundItem.exportToFile(fileURI)

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the path and name of the exported file.

#### Returns

A Boolean value of true if the file was exported successfully; false otherwise.

#### Description

Method; exports the specified item to a WAV or MP3 file. Export settings are based on the item being exported.
When exporting sound items, you should check if the soundItem.originalCompressionType property is equal to"RAW." If this check is false, you can only export the file as MP3. (Optionally, you can try exporting as a WAV file, and if the function returns false, then try to export to MP3.)

#### Example

```
Assuming that the first item in the Library is a sound item, the following code exports it as a WAV file:
var soundFileURL = "file:///C\|/out.wav";
var libItem = fl.getDocumentDOM().library.items\[0\]; libItem.exportToFile(soundFileURL);

```