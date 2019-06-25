## soundItem.convertStereoToMono

#### Availability

> Flash MX 2004.

#### Usage

> soundItem.convertStereoToMono

#### Description

> Property; a Boolean value available only for MP3 and Raw compression types. Setting this value to true converts a stereo sound to mono; false leaves it as stereo. For the MP3 compression type, if soundItem.bitRate is less than 20 Kbps, this property is ignored and forced to true (see [soundItem.bitRate](#_bookmark829)).
>
> If you want to specify a value for this property, set [soundItem.useImportedMP3Quality](#_bookmark842) to false.

#### Example

> The following example converts an item in the library to mono only if the item has the MP3 or Raw compression type:
>
> fl.getDocumentDOM().library.items\[0\].convertStereoToMono = true;

#### See also

> [soundItem.compressionType](#_bookmark831)
