## document.space()

#### Availability

Flash MX 2004.

#### Usage

document.space(direction \[, bUseDocumentBounds\])

#### Parameters

**direction** A string that specifies the direction in which to space the objects in the selection. Acceptable values are
"horizontal" or "vertical".
**bUseDocumentBounds** A Boolean value that, when set to true*,* spaces the objects to the document bounds. Otherwise, the method uses the bounds of the selected objects. The default is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; spaces the objects in the selection evenly.

#### Example

```javascript
The following example spaces the objects horizontally, relative to the Stage:
fl.getDocumentDOM().space("horizontal",true);
The following example spaces the objects horizontally, relative to each other:
fl.getDocumentDOM().space("horizontal");
The following example spaces the objects horizontally, relative to each other, with *bUseDcoumentBounds* expressly set to false:
fl.getDocumentDOM().space("horizontal",false);

```
#### See also

[document.getAlignToDocument()](../Document_object/docume72.md), [document.setAlignToDocument()](../Document_object/docum450.md)
