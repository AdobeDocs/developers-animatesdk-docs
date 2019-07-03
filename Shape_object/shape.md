## shape.beginEdit()

#### Availability

Flash MX 2004.

#### Usage

shape.beginEdit()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; defines the start of an edit session. You must use this method before issuing any commands that change the Shape object or any of its subordinate parts.

#### Example

```
The following example takes the currently selected shape and removes the first edge in the edge array from it:
var shape = fl.getDocumentDOM().selection\[0\]; shape.beginEdit();
shape.deleteEdge(0); shape.endEdit();

```