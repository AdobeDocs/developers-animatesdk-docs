## soundItem summary

**Inheritance** [Item object](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item_summary.md) \SoundItem object

#### Availability

Flash MX 2004.

#### Description

The SoundItem object is a subclass of the Item object. It represents a library item used to create a sound. See also
[frame.soundLibraryItem](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame31.md) and [Item object](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, the SoundItem object has the following method:

| **Method**                                | **Description**                                                           |
|-------------------------------------------|---------------------------------------------------------------------------|
| [soundItem.exportToFile()](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte4.md) | Exports the specified item to an MP3 or WAV file (Macintosh and Windows). |

#### Property summary

In addition to the Item object properties, the following properties are available for the SoundItem object:

| **Property**                                       | **Description**                                                                                                                                                                                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.bitRate](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundItem.md)            | A string that specifies the bit rate of a sound in the library. Available only for the MP3 compression type.                                                                                                                                    |
| [soundItem.bits](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte1.md)                    | A string that specifies the bits value for a sound in the library that has ADPCM compression.                                                                                                                                                   |
| [soundItem.compressionType](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte2.md)         | A string that specifies the compression type for a sound in the library.                                                                                                                                                                        |
| [soundItem.convertStereoToMono](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte3.md)     | A Boolean value available only for MP3 and Raw compression types.                                                                                                                                                                               |
| [soundItem.fileLastModifiedDate](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte5.md)    | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [soundItem.lastModifiedDate](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte6.md)        | Read-only; the modification date of the sound item in the Library.                                                                                                                                                                              |
| [soundItem.originalCompressionType](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte7.md) | Read-only; a string that specifies whether the specified item was imported as an MP3 file.                                                                                                                                                      |
| [soundItem.quality](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte8.md)                 | A string that specifies the playback quality of a sound in the library. Available only for the MP3 compression type.                                                                                                                            |
| [soundItem.sampleRate](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte9.md)              | A string that specifies the sample rate for the audio clip.                                                                                                                                                                                     |
| [soundItem.sourceFileExists](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIt10.md)        | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |

| **Property**                                     | **Description**                                                                                                                                                              |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.sourceFileIsCurrent](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIt11.md)   | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date on disk of the file that was imported. |
| [soundItem.sourceFilePath](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIt12.md)        | Read-only; a string, expressed as a file:/// URI, that represents the path and name of the file that was imported into the Library.                                          |
| [soundItem.useImportedMP3Quality](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIt13.md) | A Boolean value; if true, all other properties are ignored, and the imported MP3 quality is used.                                                                            |

<span id="soundItem.bitRate" class="anchor"></span>

