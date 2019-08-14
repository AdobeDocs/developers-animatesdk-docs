## fill.focalPoint

#### Availability

Flash 8.

#### Usage

fill.focalPoint

#### Description

Property; an integer that specifies the gradient focal point horizontal offset from the transformation point. A value of 10, for example, would place the focal point at 10/255 of the distance from the transformation point to the edge of the gradient. A value of -255 would place the focal point at the left boundary of the gradient. The default value is 0.
This property is available only if the value of the [fill.style](#!AdobeDocs/developers-animatesdk-docs/master/Fill_object/fill9.md) property is "radialGradient".

#### Example

```javascript
The following example sets the focal point of a radial gradient for the current selection to 100 pixels to the right of the shape’s center:
var fill = fl.getDocumentDOM().getCustomFill(); fill.style = "radialGradient";
fill.colorArray = \["\#00ff00","\#ff00ff"\]; fill.posArray = \[0, 255\];
fill.focalPoint = 10100; fl.getDocumentDOM().setCustomFill(fill);

```