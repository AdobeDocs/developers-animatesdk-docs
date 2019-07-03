## stroke.dash1

#### Availability

Flash MX 2004.

#### Usage

stroke.dash1

#### Description

Property; an integer that specifies the lengths of the solid parts of a dashed line. This property is available only if the
>
stroke.style property is set to dashed(see [stroke.style](#_bookmark898)).

#### Example

```
The following example sets the dash1 and dash2 properties for a stroke style of dashed:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "dashed";
myStroke.dash1 = 1;
myStroke.dash2 = 2; fl.getDocumentDOM().setCustomStroke(myStroke);

```