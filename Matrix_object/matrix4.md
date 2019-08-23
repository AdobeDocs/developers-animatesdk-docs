## matrix.tx

#### Availability

Flash MX 2004.

#### Usage

matrix.tx

#### Description

Property; a floating-point value that specifies the *x*-axis location of a symbol’s registration point (also *origin point* or
*zero point*) or the center of a shape. It defines the *x* translation of the transformation.
You can move an object by setting the matrix.tx and matrix.ty properties (see [matrix.ty](#!AdobeDocs/developers-animatesdk-docs/master/Matrix_object/matrix5.md)).

#### Example

```javascript
In the following example, setting tx and ty to 0 moves the registration point of the object to point 0,0 in the document:
var mat = fl.getDocumentDOM().selection\[0\].matrix; mat.tx = 0;
mat.ty = 0; fl.getDocumentDOM().selection\[0\].matrix = mat;

<span id="matrix.ty" class="anchor"></span
```