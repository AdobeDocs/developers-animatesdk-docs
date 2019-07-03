## parameter.listIndex

#### Availability

Flash MX 2004.

#### Usage

parameter.listIndex

#### Description

Property; the value of the selected list item. This property is valid only if parameter.valueType is "List".

#### Example

```
The following example sets the first parameter for a Slide, which is the autoKeyNav parameter. To set the parameter to one of its acceptable values (true, false, or inherit) parameter.listIndex is set to the index of the item in the list (0 for true, 1 for false, 2 for inherit).
var parms = fl.getDocumentDOM().screenOutline.screens\[1\].parameters; parms\[0\].listIndex = 1;

```