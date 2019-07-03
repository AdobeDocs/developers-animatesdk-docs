## matrix.b

#### Availability

Flash MX 2004.

#### Usage

matrix.b

#### Description

Property; a floating-point value that specifies the (0,1) element in the matrix. This value represents the vertical skew of a shape; it causes Flash to move the shape’s right edge along the vertical axis.
The matrix.b and matrix.c properties in a matrix represent skewing (see [matrix.c](#matrix.c)).

#### Example

```
In the following example, you can set b and c to -1 and 0, respectively; these settings skew the object at a 45º vertical angle:
var mat = fl.getDocumentDOM().selection\[0\].matrix; mat.b = -1;
mat.c = 0; fl.getDocumentDOM().selection\[0\].matrix = mat;
To skew the object back to its original shape, you can set b and c to 0. See also the [matrix.a](#_bookmark727) example.

<span id="matrix.c" class="anchor"></span
```