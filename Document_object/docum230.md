## document.punch()

#### Availability

Flash 8.

#### Usage

document.punch()

#### Parameters

None.

#### Returns

None.

#### Description

Method; uses the top selected drawing object to punch through all selected drawing objects underneath it. If no objects are selected, calling this method results in an error and the script breaks at that point.

#### Example

```javascript
The following example punches through drawing objects underneath the selected drawing object:
fl.getDocumentDOM().punch();

```
#### See also

[document.crop()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume37.md), [document.deleteEnvelope()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume41.md), [document.intersect()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume97.md), [document.union()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docu6120.md), [shape.isDrawingObject](#!AdobeDocs/developers-animatesdk-docs/master/Shape_object/shape6.md)
