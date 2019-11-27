## layer.locked

#### Availability

Flash MX 2004.

#### Usage

layer.locked

#### Description

Property; a Boolean value that specifies the locked status of the layer. If set to true, the layer is locked. The default value is false.

#### Example

```javascript
The following example stores the Boolean value for the status of the first layer in the lockStatus variable:

var lockStatus = fl.getDocumentDOM().getTimeline().layers[0].locked;
The following example sets the status of the first layer to unlocked:
fl.getDocumentDOM().getTimeline().layers[0].locked = false;
```