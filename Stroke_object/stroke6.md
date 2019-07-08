## stroke.density

#### Availability

Flash MX 2004.

#### Usage

stroke.density

#### Description

Property; a string that specifies the density of a stippled line. This property is available only if the stroke.style property is set to stipple (see [stroke.style](#_bookmark898)). Acceptable values are "very dense", "dense", "sparse", and "very sparse".

#### Example

```javascript
The following example sets the density property to sparse for the stroke style of stipple:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "stipple";
myStroke.dotSpace= 3; myStroke.variation = "random sizes"; myStroke.density = "sparse";
fl.getDocumentDOM().setCustomStroke(myStroke);

```