## stroke.breakAtCorners

#### Availability

Flash MX 2004. Deprecated in Flash CS3 in favor of [stroke.joinType](#_bookmark889).

#### Usage

stroke.breakAtCorners

#### Description

Property; a Boolean value. This property is the same as the Sharp Corners setting in the custom Stroke Style dialog box.

#### Example

```
The following example sets the breakAtCorners property to true:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.breakAtCorners = true; fl.getDocumentDOM().setCustomStroke(myStroke);

```