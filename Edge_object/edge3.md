## edge.id

#### Availability

Flash MX 2004.

#### Usage

edge.id

#### Description

Read-only property; an integer that represents a unique identifier for the edge.

#### Example

The following example stores a unique identifier for the specified edge in the my_shape_id variable:
```javascript
var shape = fl.getDocumentDOM().selection[0];
var my_shape_id = shape.edges[0].id;

```