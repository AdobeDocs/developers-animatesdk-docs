## videoItem summary

**Inheritance** [Item object](#_bookmark658) \VideoItem object

#### Availability

Flash MX 2004.

#### Description

The VideoItem object is a subclass of the [Item object](#_bookmark658).

#### Method summary

In addition to the Item object methods, the VideoItem object has the following method:

| **Property**                                        | **Description**                            |
|-----------------------------------------------------|--------------------------------------------|
| [videoItem.exportToFLV()](#videoItem.exportToFLV()) | Exports the specified item to an FLV file. |

#### Property summary

In addition to the Item object properties, you can use the following properties with the VideoItem object:

| **Property**                                     | **Description**                                                                                                                                                                                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [videoItem.fileLastModifiedDate](#_bookmark1143) | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [videoItem.lastModifiedDate](#_bookmark1144)     | Read-only; the modification date of the video item in the Library.                                                                                                                                                                              |
| [videoItem.sourceFileExists](#_bookmark1145)     | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |
| [videoItem.sourceFileIsCurrent](#_bookmark1146)  | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date (on disk) of the file that was imported.                                                                  |
| [videoItem.sourceFilePath](#_bookmark1147)       | Read-only; a string that specifies the path to the video item.                                                                                                                                                                                  |
| [videoItem.videoType](#_bookmark1148)            | Read-only; a string that specifies the type of video the item represents.                                                                                                                                                                       |

<span id="videoItem.exportToFLV()" class="anchor"></span>

