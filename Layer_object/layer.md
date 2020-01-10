## layer.animationType

#### Availability

Flash Pro CS6.

#### Usage

layer.animationType

#### Description

Read-only property; a string value indicating the animation type of the layer. Possible values include: "none", "motion object", "IK pose".

#### Example

The following example returns the layer type of the first layer of the root timeline:

```javascript
var layer = fl.getDocumentDOM().getTimeline().layers[0];
fl.trace("animationType: " + layer.animationType);
```