## shape.isOvalObject

#### Availability

Flash CS3 Professional.

#### Usage

shape.isOvalObject

#### Description

Read-only property; if true, the shape is a primitive Oval object (was created using the Oval Primitive tool).

#### Example

```
The following example displays "true" if the first selected item is a primitive Oval object, and "false" if it is not:
var sel = fl.getDocumentDOM().selection\[0\]; fl.trace(sel.isOvalObject);

```
#### See also

[shape.isRectangleObject](#shape.isRectangleObject)

<span id="shape.isRectangleObject" class="anchor"></span>
