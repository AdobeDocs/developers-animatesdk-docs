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

[document.crop()](#_bookmark159), [document.intersect()](#_bookmark229), [document.punch()](#_bookmark250), [document.union()](#_bookmark336), [shape.isDrawingObject](#_bookmark816)
