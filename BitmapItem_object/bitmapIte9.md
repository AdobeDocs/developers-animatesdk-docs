## bitmapItem.sourceFileExists

#### Availability

Flash CS4 Professional.

#### Usage

bitmapItem.sourceFileExists

#### Description

Read-only property; a Boolean value of true if the file that was imported to the Library still exists in the location from where it was imported; false otherwise.

#### Example

```javascript
Assuming the first item in the Library is a bitmap item, the following code displays "true" if the file that was imported into the Library still exists.
var libItem = fl.getDocumentDOM().library.items\[0\]; fl.trace("sourceFileExists = "+ libItem.sourceFileExists);

```
#### See also

[bitmapItem.sourceFileIsCurrent](#!AdobeDocs/developers-animatesdk-docs/test/BitmapItem_object/bitmapIt10.md), [bitmapItem.sourceFilePath](#!AdobeDocs/developers-animatesdk-docs/test/BitmapItem_object/bitmapIt11.md)

<span id="bitmapItem.sourceFileIsCurrent" class="anchor"></span>
