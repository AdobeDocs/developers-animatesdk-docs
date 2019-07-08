## shape.numCubicSegments

#### Availability

Flash CS4 Professional.

#### Usage

shape.numCubicSegments

#### Description

Read-only property; the number of cubic segments in the shape.

#### Example

```javascript
Assuming a square or rectangle shape is selected, the following code displays "4" in the Output panel:
var theShape = fl.getDocumentDOM().selection\[0\]; fl.trace(theShape.numCubicSegments);

```