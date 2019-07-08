## edge.stroke

#### Availability

Flash CS4 Professional.

#### Usage

edge.stroke

#### Description

Property; a [Stroke object](#_bookmark876).

#### Example

```javascript
The following example displays the stroke color of the first edge of the selected object:
var shape = fl.getDocumentDOM().selection\[0\]; fl.trace(shape.edges\[0\].stroke.color);

```