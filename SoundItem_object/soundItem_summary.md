## soundItem summary

**Inheritance** [Item object](#_bookmark658) \SoundItem object

#### Availability

Flash MX 2004.

#### Description

The SoundItem object is a subclass of the Item object. It represents a library item used to create a sound. See also
[frame.soundLibraryItem](#_bookmark631) and [Item object](#_bookmark658).

#### Method summary

In addition to the Item object methods, the SoundItem object has the following method:

| **Method**                                | **Description**                                                           |
|-------------------------------------------|---------------------------------------------------------------------------|
| [soundItem.exportToFile()](#_bookmark833) | Exports the specified item to an MP3 or WAV file (Macintosh and Windows). |

#### Property summary

In addition to the Item object properties, the following properties are available for the SoundItem object:

| **Property**                                       | **Description**                                                                                                                                                                                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.bitRate](#soundItem.bitRate)            | A string that specifies the bit rate of a sound in the library. Available only for the MP3 compression type.                                                                                                                                    |
| [soundItem.bits](#_bookmark830)                    | A string that specifies the bits value for a sound in the library that has ADPCM compression.                                                                                                                                                   |
| [soundItem.compressionType](#_bookmark831)         | A string that specifies the compression type for a sound in the library.                                                                                                                                                                        |
| [soundItem.convertStereoToMono](#_bookmark832)     | A Boolean value available only for MP3 and Raw compression types.                                                                                                                                                                               |
| [soundItem.fileLastModifiedDate](#_bookmark834)    | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [soundItem.lastModifiedDate](#_bookmark835)        | Read-only; the modification date of the sound item in the Library.                                                                                                                                                                              |
| [soundItem.originalCompressionType](#_bookmark836) | Read-only; a string that specifies whether the specified item was imported as an MP3 file.                                                                                                                                                      |
| [soundItem.quality](#_bookmark837)                 | A string that specifies the playback quality of a sound in the library. Available only for the MP3 compression type.                                                                                                                            |
| [soundItem.sampleRate](#_bookmark838)              | A string that specifies the sample rate for the audio clip.                                                                                                                                                                                     |
| [soundItem.sourceFileExists](#_bookmark839)        | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |

| **Property**                                     | **Description**                                                                                                                                                              |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [soundItem.sourceFileIsCurrent](#_bookmark840)   | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date on disk of the file that was imported. |
| [soundItem.sourceFilePath](#_bookmark841)        | Read-only; a string, expressed as a file:/// URI, that represents the path and name of the file that was imported into the Library.                                          |
| [soundItem.useImportedMP3Quality](#_bookmark842) | A Boolean value; if true, all other properties are ignored, and the imported MP3 quality is used.                                                                            |

<span id="soundItem.bitRate" class="anchor"></span>

