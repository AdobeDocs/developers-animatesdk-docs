## videoItem summary

**Inheritance** [Item object](../Item_object/item_summary.md) > VideoItem object

#### Availability

Flash MX 2004.

#### Description

The VideoItem object is a subclass of the [Item object](../Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, the VideoItem object has the following method:

| **Property**                                        | **Description**                            |
|-----------------------------------------------------|--------------------------------------------|
| [videoItem.exportToFLV()](../VideoItem_object/videoItem.md) | Exports the specified item to an FLV file. |

#### Property summary

In addition to the Item object properties, you can use the following properties with the VideoItem object:

| **Property**                                     | **Description**                                                                                                                                                                                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [videoItem.fileLastModifiedDate](../VideoItem_object/videoIte1.md) | Read-only; a string containing a hexadecimal number that represents the number of seconds that have elapsed between January 1, 1970, and the modification date of the original file (on disk) at the time the file was imported to the library. |
| [videoItem.lastModifiedDate](../VideoItem_object/videoIte2.md)     | Read-only; the modification date of the video item in the Library.                                                                                                                                                                              |
| [videoItem.sourceFileExists](../VideoItem_object/videoIte3.md)     | Read-only; a Boolean value that specifies whether the file that was imported to the Library still exists in the location from where it was imported.                                                                                            |
| [videoItem.sourceFileIsCurrent](../VideoItem_object/videoIte4.md)  | Read-only; a Boolean value that specifies whether the file modification date of the Library item is the same as the modification date (on disk) of the file that was imported.                                                                  |
| [videoItem.sourceFilePath](../VideoItem_object/videoIte5.md)       | Read-only; a string that specifies the path to the video item.                                                                                                                                                                                  |
| [videoItem.videoType](../VideoItem_object/videoIte6.md)            | Read-only; a string that specifies the type of video the item represents.                                                                                                                                                                       |

<span id="videoItem.exportToFLV()" class="anchor"></span>

