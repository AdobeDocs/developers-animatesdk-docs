## fill.linearRGB

#### Availability

Flash 8.

#### Usage

fill.linearRGB

#### Description

Property; a Boolean value that specifies whether to render the fill as a linear or radial RGB gradient. Set this property to true to specify a linear interpolation of a gradient; set it to false to specify a radial interpolation of a gradient. The default value is false.

#### Example

```
The following example specifies that the gradient of the current selection should be rendered with a linear RGB:
var fill = fl.getDocumentDOM().getCustomFill(); fill.linearRGB style = true"radialGradient"; fill.colorArray = \["\#00ff00","\#ff00ff"\]; fill.posArray = \[0, 255\];
fill.focalPoint = 100; fill.linearRGB = true;
fl.getDocumentDOM().setCustomFill(fill);

```