## layer.frameCount

#### Availability

Flash MX 2004.

#### Usage

layer.frameCount

#### Description

Read-only property; an integer that specifies the number of frames in the layer.

#### Example

```javascript
The following example stores the number of frames in the first layer in the fcNum variable:
var fcNum = fl.getDocumentDOM().getTimeline().layers\[0\].frameCount;

```