## document.crop()

#### Availability

Flash 8.

#### Usage

document.crop()

#### Parameters

None.

#### Returns

None.

#### Description

Method; uses the top selected drawing object to crop all selected drawing objects underneath it. If no objects are selected, calling this method results in an error and the script breaks at that point.

#### Example

```
The following example crops the currently selected objects:
fl.getDocumentDOM().crop();

```
#### See also

[document.deleteEnvelope()](#_bookmark164), [document.intersect()](#_bookmark229), [document.punch()](#_bookmark250), [document.union()](#_bookmark336), [shape.isDrawingObject](#_bookmark816)
