## soundItem.compressionType

#### Availability

Flash MX 2004.

#### Usage

soundItem.compressionType

#### Description

Property; a string that specifies that compression type for a sound in the library. Acceptable values are "Default", "ADPCM", "MP3", "Raw", and "Speech".
If you want to specify a value for this property, set [soundItem.useImportedMP3Quality](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt13.md) to false.

#### Example

```javascript
The following example changes an item in the library to compression type Raw: fl.getDocumentDOM().library.items\[0\].compressionType = "Raw";
The following example changes the compression type of the selected library items to Speech: fl.getDocumentDOM().library.getSelectedItems().compressionType = "Speech";

```
#### See also

[soundItem.originalCompressionType](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIte7.md)
