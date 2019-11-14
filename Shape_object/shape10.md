## shape.isRectangleObject

#### Availability

Flash CS3 Professional.

#### Usage

shape.isRectangleObject

#### Description

Read-only property; if true, the shape is a primitive Rectangle object (was created using the Rectangle Primitive tool).

#### Example

```javascript
The following example displays "true" if the first selected item is a primitive Rectangle object, "false" if it is not:
var sel = fl.getDocumentDOM().selection\[0\]; fl.trace(sel.isRectangleObject);

```
#### See also

[shape.isOvalObject](../Shape_object/shape9.md)
