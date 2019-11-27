## Math.concatMatrix()

#### Availability

Flash MX 2004.

#### Usage

Math.concatMatrix(mat1, mat2)

#### Parameters

**mat1, mat2** Specify the Matrix objects to be concatenated (see [Matrix object](../Matrix_object/matrix_summary.md)). Each parameter must be an object with fields a, b, c, d, tx, and ty.

#### Returns

A concatenated object matrix.

#### Description

Method; performs a matrix concatenation and returns the result.

#### Example

```javascript
The following example stores the currently selected object in the elt variable, multiplies the object matrix by the view matrix, and stores that value in the mat variable:

var elt = fl.getDocumentDOM().selection[0];
var mat = fl.Math.concatMatrix( elt.matrix , fl.getDocumentDOM().viewMatrix );

```