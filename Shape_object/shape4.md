## shape.endEdit()

#### Availability

Flash MX 2004.

#### Usage

shape.endEdit()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; defines the end of an edit session for the shape. All changes made to the Shape object or any of its subordinate parts will be applied to the shape. You must use this method after issuing any commands that change the Shape object or any of its subordinate parts.

#### Example

```javascript
The following example takes the currently selected shape and removes the first edge in the edge array from it:
var shape = fl.getDocumentDOM().selection\[0\]; shape.beginEdit();
shape.deleteEdge(0); shape.endEdit();

```