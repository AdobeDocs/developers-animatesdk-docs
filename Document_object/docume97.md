## document.intersect()

#### Availability

Flash 8.

#### Usage

document.intersect()

#### Parameters

None.

#### Returns

None.

#### Description

Method; creates an intersection drawing object from all selected drawing objects. If no objects are selected, calling this method results in an error and the script breaks at that point.

#### Example

```javascript
The following example creates an intersection drawing object from all selected drawing objects:
fl.getDocumentDOM().intersect();

```
#### See also

[document.crop()](../Document_object/docume37.md), [document.deleteEnvelope()](../Document_object/docume41.md), [document.punch()](../Document_object/docum230.md), [document.union()](../Document_object/docu6120.md), [shape.isDrawingObject](../Shape_object/shape6.md)
