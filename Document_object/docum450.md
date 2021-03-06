## document.setAlignToDocument()

#### Availability

Flash MX 2004.

#### Usage

document.setAlignToDocument(bToStage)

#### Parameters

**bToStage** A Boolean value that, if set to true, aligns objects to the Stage. If set to false, it does not.

#### Returns

Nothing.

#### Description

Method; sets the preferences for [document.align()](../Document_object/docume13.md), [document.distribute()](../Document_object/docume49.md), [document.match()](../Document_object/docum120.md), and [document.space()](../Document_object/docum67.md) to act on the document. This method is equivalent to enabling the To Stage button in the Align panel.

#### Example

The following example enables the To Stage button in the Align panel to align objects with the Stage:

```javascript
fl.getDocumentDOM().setAlignToDocument(true);

```
#### See also

[document.getAlignToDocument()](../Document_object/docume72.md)
