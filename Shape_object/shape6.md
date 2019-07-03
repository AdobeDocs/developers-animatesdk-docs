## shape.isDrawingObject

#### Availability

Flash 8.

#### Usage

shape.isDrawingObject

#### Description

Read-only property; if true, the shape is a drawing object.

#### Example

```
The following example stores the first selected object in the sel variable and then uses the [element.elementType](#_bookmark378) and
shape.isDrawingObject properties to determine if the selected item is a drawing object:
var sel = fl.getDocumentDOM().selection\[0\];
var shapeDrawingObject = (sel.elementType == "shape") && sel.isDrawingObject; fl.trace(shapeDrawingObject);

```
#### See also

[document.crop()](#_bookmark160), [document.deleteEnvelope()](#_bookmark165), [document.intersect()](#_bookmark230), [document.punch()](#_bookmark251), [document.union()](#_bookmark337), [shape.isGroup](#_bookmark818)
