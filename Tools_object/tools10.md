## tools.snapPoint()

#### Availability

Flash MX 2004.

#### Usage

tools.snapPoint(pt)

#### Parameters

**pt** Specifies the location of the point for which you want to return a snap point.

#### Returns

A new point that may be adjusted or snapped to the nearest geometric object.

#### Description

Method; takes a point as input and returns a new point that may be adjusted or *snapped* to the nearest geometric object. If snapping is disabled in the View menu in the Flash user interface, the point returned is the original point.

#### Example

```javascript
The following example returns a new point that may be snapped to the nearest geometric object.
var theSnapPoint = fl.tools.snapPoint(pt1);

```