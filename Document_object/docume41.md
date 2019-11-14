## document.deleteEnvelope()

#### Availability

Flash 8.

#### Usage

document.deleteEnvelope()

#### Parameters

None.

#### Returns

None.

#### Description

Method; deletes the envelope (bounding box that contains one or more objects) from the selected objects. If no objects are selected, calling this method results in an error and the script breaks at that point.

#### Example

```javascript
The following example deletes the envelope from the selected objects:
fl.getDocumentDOM().deleteEnvelope();

```
#### See also

[document.crop()](../Document_object/docume37.md), [document.intersect()](../Document_object/docume97.md), [document.punch()](../Document_object/docum230.md), [document.union()](../Document_object/docu6120.md), [shape.isDrawingObject](../Shape_object/shape6.md)
