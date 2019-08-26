## soundItem.sampleRate

#### Availability

Flash MX 2004.

#### Usage

soundItem.sampleRate

#### Description

Property; a string that specifies the sample rate for the audio clip. This property is available only for the ADPCM, Raw, and Speech compression types. Acceptable values are "5 kHz", "11 kHz", "22 kHz", and "44 kHz".
If you want to specify a value for this property, set [soundItem.useImportedMP3Quality](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt13.md) to false.

#### Example

```javascript
The following example sets the sample rate of an item in the library to 5 kHz if the item has the ADPCM, Raw, or Speech compression type:
fl.getDocumentDOM().library.items\[0\].sampleRate = "5 kHz";

```
#### See also

[soundItem.compressionType](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIte2.md)
