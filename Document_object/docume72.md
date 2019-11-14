## document.getAlignToDocument()

#### Availability

Flash MX 2004.

#### Usage

document.getAlignToDocument()

#### Parameters

None.

#### Returns

A Boolean value: true if the preference is set to align the objects to the Stage; false otherwise.

#### Description

Method; identical to retrieving the value of the To Stage button in the Align panel. Gets the preference that can be used for [document.align()](../Document_object/docume13.md), [document.distribute()](../Document_object/docume49.md), [document.match()](../Document_object/docum120.md), and [document.space()](../Document_object/docum67.md) methods on the document.

#### Example

```javascript
The following example retrieves the value of the To Stage button in the Align panel. If the return value is true, the To Stage button is active; otherwise, it is not.
var isAlignToDoc = fl.getDocumentDOM().getAlignToDocument(); fl.getDocumentDOM().align("left", isAlignToDoc);

```
#### See also

[document.setAlignToDocument()](../Document_object/docum450.md)
