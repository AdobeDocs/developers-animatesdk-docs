## document.getSelectionRect()

#### Availability

Flash MX 2004.

#### Usage

document.getSelectionRect()

#### Parameters

None.

#### Returns

The bounding rectangle of the current selection, or 0 if nothing is selected. For information on the format of the return value, see [document.addNewRectangle()](../Document_object/docume10.md).

#### Description

Method; gets the bounding rectangle of the current selection. If a selection is non-rectangular, the smallest rectangle encompassing the entire selection is returned. The rectangle is based on the document space or, when in edit mode, the registration point (also *origin point* or *zero point*) of the symbol being edited.

#### Example

```javascript
The following example gets the bounding rectangle for the current selection and then displays its properties:
var newRect = fl.getDocumentDOM().getSelectionRect();
var outputStr = "left: " + newRect.left + " top: " + newRect.top + " right: " + newRect.right
\+ " bottom: " + newRect.bottom; alert(outputStr);

```
#### See also

[document.selection](../Document_object/docum430.md), [document.setSelectionRect()](../Document_object/docu9689.md)
