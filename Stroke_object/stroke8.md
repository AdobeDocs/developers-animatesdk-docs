## stroke.dotSpace

#### Availability

Flash MX 2004.

#### Usage

stroke.dotSpace

#### Description

Property; an integer that specifies the spacing between dots in a dotted line. This property is available only if the
stroke.style property is set to dotted. See [stroke.style](#!AdobeDocs/developers-animatesdk-docs/test/Stroke_object/stroke20.md).

#### Example

```javascript
The following example sets the dotSpace property to 3 for a stroke style of dotted:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "dotted";
myStroke.dotSpace= 3; fl.getDocumentDOM().setCustomStroke(myStroke);

```