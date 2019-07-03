## document.match()

#### Availability

Flash MX 2004.

#### Usage

document.match(bWidth, bHeight \[, bUseDocumentBounds\])

#### Parameters

**bWidth** A Boolean value that, when set to true, causes the method to make the widths of the selected items the same.
**bHeight** A Boolean value that, when set to true, causes the method to make the heights of the selected items the same.
**bUseDocumentBounds** A Boolean value that, when set to true, causes the method to match the size of the objects to the bounds of the document. Otherwise, the method uses the bounds of the largest object. The default is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; makes the size of the selected objects the same.

#### Example

```
The following example matches the width of the selected objects only:
fl.getDocumentDOM().match(true,false); The following example matches the height only: fl.getDocumentDOM().match(false,true);
The following example matches the width only to the bounds of the document:
fl.getDocumentDOM().match(true,false,true);

```
#### See also

[document.getAlignToDocument()](#_bookmark198), [document.setAlignToDocument()](#_bookmark277)
