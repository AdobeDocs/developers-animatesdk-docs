## element.getTransformationPoint()

#### Availability

Flash CS3 Professional.

#### Usage

element.getTransformationPoint()

#### Parameters

None.

#### Returns

A point (for example, {x:10, y:20}, where x and y are floating-point numbers) that specifies the position of the transformation point (also *origin point* or *zero point*) within the element’s coordinate system.

#### Description

Method; gets the value of the specified element’s transformation point.
Transformation points are relative to different locations, depending on the type of item selected. For more information, see [element.setTransformationPoint()](#_bookmark400).

#### Example

```
The following example gets the transformation point for the third element in the ninth frame on the first layer in the document. The transPoint.x property gives the *x* coordinate of the transformation point. The transPoint.y property gives the *y* coordinate of the transformation point.
var transPoint = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[8\].elements\[2\].getTransformationPoint();

```
#### See also

[document.getTransformationPoint()](#_bookmark219), [element.setTransformationPoint()](#_bookmark400), [element.transformX](#_bookmark406), [element.transformY](#_bookmark407)
