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

```javascript
The following example crops the currently selected objects:
fl.getDocumentDOM().crop();

```
#### See also

[document.deleteEnvelope()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume41.md), [document.intersect()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume97.md), [document.punch()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum230.md), [document.union()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docu6120.md), [shape.isDrawingObject](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape6.md)
