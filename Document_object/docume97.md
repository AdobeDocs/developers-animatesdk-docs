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

[document.crop()](#_bookmark159), [document.deleteEnvelope()](#_bookmark164), [document.punch()](#_bookmark250), [document.union()](#_bookmark336), [shape.isDrawingObject](#_bookmark816)
