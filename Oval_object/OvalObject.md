## OvalObject.closePath

#### Availability

Flash CS3 Professional.

#### Usage

OvalObject.closePath

#### Description

Read-only property; a Boolean value that specifies whether the Close Path check box in the Property inspector is selected. If the start angle and end angle values for the object are the same, setting this property has no effect until the values change.
To set this value, use [document.setOvalObjectProperty()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum590.md).

#### Example

```javascript
The following example deselects the OvalObject.closePath property:
fl.getDocumentDOM().setOvalObjectProperty("closePath",false);

```
#### See also

[document.setOvalObjectProperty()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum590.md), [shape.isOvalObject](#!AdobeDocs/developers-animatesdk-docs/test/Shape_object/shape9.md)
