## stroke.hatchThickness

#### Availability

Flash MX 2004.

#### Usage

stroke.hatchThickness

#### Description

Property; a string that specifies the thickness of a hatch line. This property is available only if the stroke.style
>
property is set to hatched (see [stroke.style](#_bookmark898)). Acceptable values are "hairline", "thin", "medium", and "thick".

#### Example

```
The following example sets the hatchThickness property to thin for a stroke style of hatched:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "hatched";
myStroke.curve = "straight"; myStroke.space = "close"; myStroke.jiggle = "wild"; myStroke.rotate = "free"; myStroke.length = "slight"; myStroke.hatchThickness = "thin";
fl.getDocumentDOM().setCustomStroke(myStroke);

```