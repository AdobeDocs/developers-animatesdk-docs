## bitmapItem.hasValidAlphaLayer

#### Availability

Flash CS6 Professional.

#### Usage

bitmapItem.hasValidAlphaLayer

#### Description

Read-only property; a boolean indicating if a bitmap in the library has a valid/useful alpha channel. This flag will help you decide if you should export the bitmap item as a PNG instead of a JPEG using the bitmapItem.exportToFile() function.

#### Example

```javascript
The following code exports a library item with the proper file name extension depending on whether it has a valid alpha layer.
var bitmapItem = fl.getDocumentDOM().library.items\[0\]; var uri = fl.browseForFileURI("open");
if (bitmapItem.hasValidAlphaLayer) uri += ".png"; else uri += ".jpg";
bitmapItem.exportToFile(uri);

```
#### See also

[bitmapItem.sourceFileExists](#_bookmark60), [bitmapItem.sourceFileIsCurrent](#_bookmark61), [bitmapItem.sourceFilePath](#_bookmark62), [FLfile.getModificationDate()](#_bookmark568)
