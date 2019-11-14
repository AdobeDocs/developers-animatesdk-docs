## videoItem.sourceFileIsCurrent

#### Availability

Flash CS4 Professional.

#### Usage

videoItem.sourceFileIsCurrent

#### Description

Read-only property: a Boolean value of true if the file modification date of the Library item is the same as the modification date (on disk) of the file that was imported; false otherwise.

#### Example

```javascript
Assuming that the first item in the Library is a video item, the following code displays "true" if the file that was imported has not been modified on disk since it was imported.
var libItem = fl.getDocumentDOM().library.items\[0\]; fl.trace("fileIsCurrent = "+ libItem.sourceFileIsCurrent);

```
#### See also

[videoItem.fileLastModifiedDate](../VideoItem_object/videoIte1.md), [videoItem.sourceFilePath](../VideoItem_object/videoIte5.md)

<span id="videoItem.sourceFilePath" class="anchor"></span>
