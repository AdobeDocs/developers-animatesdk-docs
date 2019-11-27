## item.itemType

#### Availability

Flash MX 2004.

#### Usage

item.itemType

#### Description

Read-only property; a string that specifies the type of element. The value is one of the following: "undefined", "component", "movie clip", "graphic", "button", "folder", "font", "sound", "bitmap", "compiled clip", "screen", or "video". If this property is "video", you can determine the type of video; see [videoItem.videoType](../VideoItem_object/videoIte6.md).

#### Example

```javascript
The following example shows the type of the specified library item in the Output panel:

fl.trace(fl.getDocumentDOM().library.items[0].itemType);

```