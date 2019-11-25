## fill.matrix

#### Availability

Flash MX 2004.

#### Usage

fill.matrix

#### Description

Property; a [Matrix object](../Matrix_object/matrix_summary.md) that defines the placement, orientation, and scales for gradient fills.

#### Example

```javascript
The following example uses the fill.matrix property to specify a gradient fill for the current selection:
var fill = fl.getDocumentDOM().getCustomFill(); fill.style = 'radialGradient';
fill.colorArray =  [' #00ff00',' #ff00ff' ]; fill.posArray =  [0, 255 ];
fill.focalPoint = 100; fill.linearRGB = false; fill.overflow = 'repeat'; var mat = fill.matrix; mat.a = 0.0167083740234375;
mat.b = -0.0096435546875;
mat.c = 0.0312957763671875;
mat.d = 0.05419921875;
mat.tx = 288.65;
mat.ty = 193.05; for (i in mat) {
fl.trace(i+' : '+mat [i]);
}
fl.getDocumentDOM().setCustomFill(fill);

```