## halfEdge.id

#### Availability

Flash MX 2004.

#### Usage

halfEdge.id

#### Description

Read-only property; a unique integer identifier for the HalfEdge object.

#### Example

The following example displays a unique identifier for the specified half edge in the Output panel:

```javascript
var shape = fl.getDocumentDOM().selection[0]; alert(shape.contours[0].getHalfEdge().id);
```