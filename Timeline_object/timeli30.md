## timeline.layerCount

#### Availability

Flash MX 2004.

#### Usage

timeline.layerCount

#### Description

Read-only property; an integer that represents the number of layers in the specified timeline.

#### Example


The following example uses the NumLayer variable to store the number of layers in the current scene:
```javascript
var NumLayer = fl.getDocumentDOM().getTimeline().layerCount;
```