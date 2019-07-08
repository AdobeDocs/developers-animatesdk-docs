## frame.labelType

#### Availability

Flash MX 2004.

#### Usage

frame.labelType

#### Description

Property; a string that specifies the type of Frame name. Acceptable values are "none", "name", "comment", and
"anchor". Setting a label to "none" clears the [frame.name](#_bookmark621) property.

#### Example

```javascript
The following example sets the name of the first frame in the top layer to "First Frame" and then sets its label to"comment":
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].name = 'First Frame'; fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].labelType = 'comment';

```