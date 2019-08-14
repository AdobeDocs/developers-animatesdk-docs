## OvalObject.startAngle

#### Availability

Flash CS3 Professional.

#### Usage

OvalObject.startAngle

#### Description

Read-only property; a float value that specifies the start angle of the Oval object. Acceptable values are from 0 to 360. To set this value, use [document.setOvalObjectProperty()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum590.md).

#### Example

```javascript
The following example sets the start angle of selected Oval objects to 270:
fl.getDocumentDOM().setOvalObjectProperty("startAngle",270);

```
#### See also

[document.setOvalObjectProperty()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum590.md), [OvalObject.endAngle](#!AdobeDocs/developers-animatesdk-docs/master/Oval_object/OvalObjec1.md), [shape.isOvalObject](#!AdobeDocs/developers-animatesdk-docs/master/Shape_object/shape9.md)
