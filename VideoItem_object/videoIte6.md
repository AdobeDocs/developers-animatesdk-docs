## videoItem.videoType

#### Availability

Flash 8.

#### Usage

videoItem.videoType

#### Description

Read-only property; a string that specifies the type of video the item represents. Possible values are "embedded video"
and "video".

#### Example

```
The following example displays the name and type of any items in the library that are of type video:
for (idx in fl.getDocumentDOM().library.items) {
if (fl.getDocumentDOM().library.items\[idx\].itemType == "video") { var myItem = fl.getDocumentDOM().library.items\[idx\]; fl.trace(myItem.name + " is " + myItem.videoType);
}
}

```