## tools.constrainPoint()

#### Availability

Flash MX 2004.

#### Usage

tools.constrainPoint(pt1, pt2)

#### Parameters

**pt1, pt2** Points that specify the starting-click point and the drag-to point.

#### Returns

A new adjusted or constrained point.

#### Description

Method; takes two points and returns a new adjusted or constrained point. If the Shift key is pressed when the command is run, the returned point is constrained to follow either a 45º constrain (useful for something such as a line with an arrowhead) or to constrain an object to maintain its aspect ratio (such as pulling out a perfect square with the Rectangle tool).

#### Example

The following example returns a constrained point:
```javascript
pt2 = fl.tools.constrainPoint(pt1, tempPt);
```