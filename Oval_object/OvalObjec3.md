## OvalObject.startAngle

#### Availability

Flash CS3 Professional.

#### Usage

OvalObject.startAngle

#### Description

Read-only property; a float value that specifies the start angle of the Oval object. Acceptable values are from 0 to 360. To set this value, use [document.setOvalObjectProperty()](#_bookmark298).

#### Example

```javascript
The following example sets the start angle of selected Oval objects to 270:
fl.getDocumentDOM().setOvalObjectProperty("startAngle",270);

```
#### See also

[document.setOvalObjectProperty()](#_bookmark298), [OvalObject.endAngle](#_bookmark744), [shape.isOvalObject](#_bookmark820)
