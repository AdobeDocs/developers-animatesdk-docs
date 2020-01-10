## edge.stroke

#### Availability

Flash CS4 Professional.

#### Usage

edge.stroke

#### Description

Property; a [Stroke object](../Stroke_object/stroke_summary.md).

#### Example

The following example displays the stroke color of the first edge of the selected object:
```javascript
var shape = fl.getDocumentDOM().selection[0];
fl.trace(shape.edges[0].stroke.color);

```