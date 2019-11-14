## stroke.curve

#### Availability

Flash MX 2004.

#### Usage

stroke.curve

#### Description

Property; a string that specifies the type of hatching for the stroke. This property can be set only if the stroke.style property is set to "hatched" (see [stroke.style](../Stroke_object/stroke20.md)). Acceptable values are "straight", "slight curve", "medium curve", and "very curved".

#### Example

```javascript
The following example sets the curve property, as well as others, for a stroke having the hatched style:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "hatched";
myStroke.curve = "straight"; myStroke.space = "close"; myStroke.jiggle = "wild"; myStroke.rotate = "free"; myStroke.length = "slight"; myStroke.hatchThickness = "thin";
fl.getDocumentDOM().setCustomStroke(myStroke);

```