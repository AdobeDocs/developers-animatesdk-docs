## soundItem.bits

#### Availability

Flash MX 2004.

#### Usage

soundItem.bits

#### Description

Property; a string that specifies the bits value for a sound in the library that has ADPCM compression. Acceptable values are "2 bit", "3 bit", "4 bit", and "5 bit".
If you want to specify a value for this property, set [soundItem.useImportedMP3Quality](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIt13.md) to false.

#### Example

```javascript
The following example displays the bits value in the Output panel if the currently selected item in the library has the ADPCM compression type:
alert(fl.getDocumentDOM().library.items\[0\].bits);

```
#### See also

[soundItem.compressionType](#!AdobeDocs/developers-animatesdk-docs/test/SoundItem_object/soundIte2.md)

<span id="soundItem.compressionType" class="anchor"></span>
