## document.getTransformationPoint()

#### Availability

Flash MX 2004.

#### Usage

document.getTransformationPoint()

#### Parameters

None.

#### Returns

A point (for example, {x:10, y:20}, where x and y are floating-point numbers) that specifies the position of the transformation point (also *origin point* or *zero point*) within the selected element’s coordinate system.

#### Description

Method; gets the location of the transformation point of the current selection. You can use the transformation point for commutations such as rotate and skew.
>
***Note:** Transformation points are relative to different locations, depending on the type of item selected. For more information, see [document.setTransformationPoint()](#_bookmark316).*

#### Example

```
The following example gets the transformation point for the current selection. The transPoint.x property gives the *x* coordinate of the transformation point. The transPoint.y property gives the *y* coordinate of the transformation point.
var transPoint = fl.getDocumentDOM().getTransformationPoint();

```
#### See also

[document.setTransformationPoint()](#_bookmark316), [element.getTransformationPoint()](#_bookmark382)
