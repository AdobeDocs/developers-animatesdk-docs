## videoItem.sourceFileExists

#### Availability

Flash CS4 Professional.

#### Usage

videoItem.sourceFileExists

#### Description

Read-only property: a Boolean value of true if the file that was imported to the Library still exists in the location from where it was imported; false otherwise.

#### Example

```javascript
Assuming that the first item in the Library is a video item, the following code displays "true" if the file that was imported into the Library still exists.
var libItem = fl.getDocumentDOM().library.items\[0\]; fl.trace("sourceFileExists = "+ libItem.sourceFileExists);

```
#### See also

[videoItem.sourceFileIsCurrent](#!AdobeDocs/developers-animatesdk-docs/test/VideoItem_object/videoIte4.md), [videoItem.sourceFilePath](#!AdobeDocs/developers-animatesdk-docs/test/VideoItem_object/videoIte5.md)

<span id="videoItem.sourceFileIsCurrent" class="anchor"></span>
