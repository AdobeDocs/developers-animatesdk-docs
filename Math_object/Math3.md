## Math.transformPoint()

#### Availability

Flash CS6.

#### Usage

Math.transformPoint(matrix, point)

#### Parameters

**matrix** Contains the matrix obejct applied to the point.
>
**point** Contains the point to which the matrix is applied.

#### Returns

The transformed point.

#### Description

Method; applies a matrix to a point.

#### Example

```
The following example gets a matrix from the first object in Frame 1, creates a point with x:100 and y:200, and transforms this point using the matrix in the first line:
var mat = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].matrix; var point = {x:100, y:200};
var retPoint = fl.Math.transformPoint(mat, point);

```