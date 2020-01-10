## matrix.a

#### Availability

Flash MX 2004.

#### Usage

matrix.a

#### Description

Property; a floating-point value that specifies the (0,0) element in the transformation matrix. This value represents the scale factor of the object’s *x*-axis.

#### Example

The a and d properties in a matrix represent scaling. In the following example, the values are set to 2 and 3, respectively, to scale the selected object to two times its width and three times its height:
```javascript
var mat = fl.getDocumentDOM().selection[0].matrix;
mat.a = 2;
mat.d = 3;
fl.getDocumentDOM().selection[0].matrix = mat;
```
You can rotate an object by setting the a, b, c, and d matrix properties relative to one another, where a = d and b =
-c. For example, values of 0.5, 0.8, -0.8, and 0.5 rotate the object 60º:
```javascript
var mat = fl.getDocumentDOM().selection[0].matrix;
mat.a = 0.5;
mat.b = 0.8;
mat.c = 0.8*(-1);
mat.d = 0.5;
fl.getDocumentDOM().selection[0].matrix = mat;
```
You can set a = d = 1 and c = b = 0 to reset the object back to its original shape.