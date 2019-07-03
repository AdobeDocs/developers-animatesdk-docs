## stroke.rotate

#### Availability

Flash MX 2004.

#### Usage

stroke.rotate

#### Description

Property; a string that specifies the rotation of a hatch line. This property is available only if the stroke.style
property is set to hatched (see [stroke.style](#_bookmark898)). Acceptable values are "none", "slight", "medium", and "free".

#### Example

```
The following example sets the rotate property to free for a style stroke of hatched:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "hatched";
myStroke.curve = "straight"; myStroke.space = "close"; myStroke.jiggle = "wild"; myStroke.rotate = "free"; myStroke.length = "slight"; myStroke.hatchThickness = "thin";

```