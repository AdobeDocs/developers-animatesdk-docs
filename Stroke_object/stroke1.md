## stroke.capType

#### Availability

Flash 8.

#### Usage

stroke.capType

#### Description

Property; a string that specifies the type of cap for the stroke. Acceptable values are "none", "round", and "square".

#### Example

```
The following example sets the stroke cap type to round:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.capType = "round"; fl.getDocumentDOM().setCustomStroke(myStroke);

```