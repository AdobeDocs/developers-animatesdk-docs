## soundItem.originalCompressionType

#### Availability

Flash CS4 Professional.

#### Usage

soundItem.originalCompressionType

#### Description

Read-only property: a string that specifies whether the specified item was imported as an mp3 file. Possible values for this property are “RAW” and “MP3”.

#### Example

```
Assuming that the first item in the Library is a sound item, the following code displays "MP3" if the file was imported into the Library as an MP3 file, or "RAW" if it was not:
var libItem = fl.getDocumentDOM().library.items\[0\];
fl.trace("Imported compression type = "+ libItem.originalCompressionType);

```
#### See also

[soundItem.compressionType](#_bookmark831)
