## bitmapItem.sourceFilePath

#### Availability

Flash CS4 Professional.

#### Usage

bitmapItem.sourceFilePath

#### Description

Read-only property; a string, expressed as a file:/// URI, that represents the path and name of the file that was imported into the Library.

#### Example

```javascript
The following example displays the name and source file path of any items in the library that are of type "bitmap":
for (idx in fl.getDocumentDOM().library.items) {
if (fl.getDocumentDOM().library.items\[idx\].itemType == "bitmap") { var myItem = fl.getDocumentDOM().library.items\[idx\]; fl.trace(myItem.name + " source is " + myItem.sourceFilePath);

}

}

```
#### See also

[bitmapItem.sourceFileExists](#!AdobeDocs/developers-animatesdk-docs/master/BitmapItem_object/bitmapIte9.md)
