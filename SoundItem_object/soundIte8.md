## soundItem.quality

#### Availability

Flash MX 2004.

#### Usage

soundItem.quality

#### Description

Property; a string that specifies the playback quality of a sound in the library. This property is available only for the MP3 compression type. Acceptable values are "Fast", "Medium", and "Best".
>
If you want to specify a value for this property, set [soundItem.useImportedMP3Quality](#_bookmark842) to false.

#### Example

```
The following example sets the playback quality of an item in the library to Best if the item has the MP3 compression type:
fl.getDocumentDOM().library.items\[0\].quality = "Best";

```
#### See also

[soundItem.compressionType](#_bookmark831)
