## soundItem.sourceFileIsCurrent

#### Availability

Flash CS4 Professional.

#### Usage

soundItem.sourceFileIsCurrent

#### Description

Read-only property: a Boolean value of true if the file modification date of the Library item is the same as the modification date on disk of the file that was imported; false otherwise.

#### Example

```javascript
Assuming that the first item in the Library is a sound item, the following code displays "true" if the file that was imported has not been modified on disk since it was imported.
var libItem = fl.getDocumentDOM().library.items\[0\]; fl.trace("fileIsCurrent = "+ libItem.sourceFileIsCurrent);

```
#### See also

[soundItem.fileLastModifiedDate](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIte5.md), [soundItem.sourceFilePath](#!AdobeDocs/developers-animatesdk-docs/master/SoundItem_object/soundIt12.md)

<span id="soundItem.sourceFilePath" class="anchor"></span>
