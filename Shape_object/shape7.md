## shape.isFloating

#### Availability

Flash CS6.

#### Usage

*shape.isFloating*

#### Description

Read-only property; if true, the shape is floating above the parent frame’s (or group’s) shape. Also, if true, this type of shape will have it's own matrix, similar to a drawing object.

#### Example

The following example displays whether a specified shape is floating:

```javascript
var myShape = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0]; 
fl.trace("is shape floating? " + myShape.isFloating);

```