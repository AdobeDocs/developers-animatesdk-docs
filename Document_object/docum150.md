## document.moveSelectedBezierPointsBy()

#### Availability

Flash MX 2004.

#### Usage

document.moveSelectedBezierPointsBy(delta)

#### Parameters

**delta** A pair of floating-point values that specify the *x* and *y* coordinates in pixels by which the selected B�zier points are moved. For example, passing ({x:1,y:2}) specifies a location that is to the right by one pixel and down by two pixels from the current location.

#### Returns

Nothing.

#### Description

Method; if the selection contains at least one path with at least one B�zier point selected, moves all selected B�zier points on all selected paths by the specified amount.

#### Example

```
The following example moves the selected B�zier points 10 pixels to the right and 5 pixels down:
fl.getDocumentDOM().moveSelectedBezierPointsBy({x:10, y:5});

```