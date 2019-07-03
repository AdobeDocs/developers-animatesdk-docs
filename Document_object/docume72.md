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

Method; identical to retrieving the value of the To Stage button in the Align panel. Gets the preference that can be used for [document.align()](#_bookmark132), [document.distribute()](#_bookmark173), [document.match()](#_bookmark237), and [document.space()](#_bookmark323) methods on the document.

#### Example

```
The following example retrieves the value of the To Stage button in the Align panel. If the return value is true, the To Stage button is active; otherwise, it is not.
var isAlignToDoc = fl.getDocumentDOM().getAlignToDocument(); fl.getDocumentDOM().align("left", isAlignToDoc);

```
#### See also

[document.setAlignToDocument()](#_bookmark277)
