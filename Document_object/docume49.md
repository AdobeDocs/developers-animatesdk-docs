## document.distribute()

#### Availability

Flash MX 2004.

#### Usage

document.distribute(distributemode [, bUseDocumentBounds])

#### Parameters

**distributemode** A string that specifies where to distribute the selected objects. Acceptable values are "left edge", "horizontal center", "right edge", "top edge", "vertical center", and "bottom edge".
**bUseDocumentBounds** A Boolean value that, when set to true, distributes the selected objects using the bounds of the document. Otherwise, the method uses the bounds of the selected objects. The default is false.

#### Returns

Nothing.

#### Description

Method; distributes the selection.

#### Example

```javascript
The following example distributes the selected objects by their top edges:
fl.getDocumentDOM().distribute("top edge");

The following example distributes the selected objects by their top edges and expressly sets the *bUseDcoumentBounds*
parameter:
fl.getDocumentDOM().distribute("top edge", false);

The following example distributes the selected objects by their top edges, using the bounds of the document:
fl.getDocumentDOM().distribute("top edge", true);

```
#### See also

[document.getAlignToDocument()](../Document_object/docume72.md), [document.setAlignToDocument()](../Document_object/docum450.md)
