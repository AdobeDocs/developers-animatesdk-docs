## edge.cubicSegmentIndex

#### Availability

Flash CS4 Professional.

#### Usage

edge.cubicSegmentIndex

#### Description

Read-only property; an integer that specifies the index value of a cubic segment of the edge (see [shape.getCubicSegmentPoints()](#!AdobeDocs/developers-animatesdk-docs/master/Shape_object/shape5.md)).

#### Example

```javascript
The following code displays the index values of all the cubic segments of the specified edge:
var theShape = fl.getDocumentDOM().selection\[0\]; var edgesArray = theShape.edges;
for(var i=0;i\<edgesArray.length; i++) { fl.trace(edgesArray\[i\].cubicSegmentIndex);
}

```