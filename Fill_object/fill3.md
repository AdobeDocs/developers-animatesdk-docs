## fill.colorArray

#### Availability

Flash MX 2004.

#### Usage

fill.colorArray

#### Description

Property; an array of colors in the gradient, expressed as integers. This property is available only if the value of the
fill.style property is either "radialGradient" or "linearGradient". See [fill.style](../Fill_object/fill9.md)

#### Example

```javascript
The following example displays the color array of the current selection, if appropriate, in the Output panel:
var fill = fl.getDocumentDOM().getCustomFill();
if(fill.style == "linearGradient" || fill.style == "radialGradient") alert(fill.colorArray);
The following example sets the fill to the specified linear gradient:
var fill = fl.getDocumentDOM().getCustomFill(); fill.style = "linearGradient";
fill.colorArray = ["#00ff00","#ff00ff"]; fill.posArray = [0, 255]; fl.getDocumentDOM().setCustomFill(fill);

```