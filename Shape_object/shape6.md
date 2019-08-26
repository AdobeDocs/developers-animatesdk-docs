## shape.isDrawingObject

#### Availability

Flash 8.

#### Usage

shape.isDrawingObject

#### Description

Read-only property; if true, the shape is a drawing object.

#### Example

```javascript
The following example stores the first selected object in the sel variable and then uses the [element.elementType](#!AdobeDocs/developers-animatesdk-docs/test/Element_object/element1.md) and
shape.isDrawingObject properties to determine if the selected item is a drawing object:
var sel = fl.getDocumentDOM().selection\[0\];
var shapeDrawingObject = (sel.elementType == "shape") && sel.isDrawingObject; fl.trace(shapeDrawingObject);

```
#### See also

[document.crop()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume37.md), [document.deleteEnvelope()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume41.md), [document.intersect()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume97.md), [document.punch()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum230.md), [document.union()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docu6120.md), [shape.isGroup](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape8.md)
