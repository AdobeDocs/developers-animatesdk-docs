## Math.pointDistance()

#### Availability

Flash MX 2004.

#### Usage

Math.pointDistance(pt1, pt2)

#### Parameters

**pt1, pt2** Specify the points between which distance is measured.

#### Returns

A floating-point value that represents the distance between the points.

#### Description

Method; computes the distance between two points.

#### Example

```javascript
The following example stores the value for the distance between *pt1* and *pt2* in the dist variable:
var pt1 = {x:10, y:20} var pt2 = {x:100, y:200}
var dist = fl.Math.pointDistance(pt1, pt2);

```