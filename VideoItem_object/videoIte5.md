## videoItem.sourceFilePath

#### Availability

Flash 8.

#### Usage

videoItem.sourceFilePath

#### Description

Read-only property; a string, expressed as a file:/// URI that specifies the path to the video item.

#### Example

```javascript
The following example displays the name and source file path of any items in the library that are of type video:
for (idx in fl.getDocumentDOM().library.items) {
if (fl.getDocumentDOM().library.items\[idx\].itemType == "video") { var myItem = fl.getDocumentDOM().library.items\[idx\]; fl.trace(myItem.name + " source is " + myItem.sourceFilePath);

}

}

```
#### See also

[videoItem.sourceFileExists](#!AdobeDocs/developers-animatesdk-docs/test/VideoItem_object/videoIte3.md)
