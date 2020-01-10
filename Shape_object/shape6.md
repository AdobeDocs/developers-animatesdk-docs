## shape.isDrawingObject

#### Availability

Flash 8.

#### Usage

*shape.isDrawingObject*

#### Description

Read-only property; if true, the shape is a drawing object.

#### Example

The following example stores the first selected object in the sel variable and then uses the [element.elementType](../Element_object/element1.md) and
shape.isDrawingObject properties to determine if the selected item is a drawing object:

```javascript
var sel = fl.getDocumentDOM().selection[0];
var shapeDrawingObject = (sel.elementType == "shape") && sel.isDrawingObject; 
fl.trace(shapeDrawingObject);

```
#### See also

[document.crop()](../Document_object/docume37.md), [document.deleteEnvelope()](../Document_object/docume41.md), [document.intersect()](../Document_object/docume97.md), [document.punch()](../Document_object/docum230.md), [document.union()](../Document_object/docu6120.md), [shape.isGroup](../Shape_object/shape8.md)
