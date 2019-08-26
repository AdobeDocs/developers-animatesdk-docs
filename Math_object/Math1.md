## Math.invertMatrix()

#### Availability

Flash MX 2004.

#### Usage

Math.invertMatrix(mat)

#### Parameters

**mat** Indicates the Matrix object to invert (see [Matrix object](#!AdobeDocs/developers-animatesdk-docs/test/Matrix_object/matrix_summary.md)). It must have the following fields: a, b, c, d, tx, and ty.

#### Returns

A Matrix object that is the inverse of the original matrix.

#### Description

Method; returns the inverse of the specified matrix.

#### Example

```javascript
The following example stores the currently selected object in the elt variable, assigns that matrix to the mat variable, and stores the inverse of the matrix in the inv variable:
var elt = fl.getDocumentDOM().selection\[0\]; var mat = elt.matrix;
var inv = fl.Math.invertMatrix( mat );

```