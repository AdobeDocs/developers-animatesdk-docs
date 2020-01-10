## layer.parentLayer

#### Availability

Flash MX 2004.

#### Usage

layer.parentLayer

#### Description

Property; a Layer object that represents the layer’s containing folder, guiding, or masking layer. The parent layer must be a folder, guide, or mask layer that precedes the layer, or the *parentLayer* of the preceding or following layer. Setting the layer’s *parentLayer* does not move the layer’s position in the list; trying to set a layer’s parentLayer to a layer that would require moving it has no effect. Uses *null* for a top-level layer.

#### Example

The following example uses two layers at the same level on the same timeline. The first layer (layers[0]) is converted
into a folder and then set as the parent folder of the second layer (layers[1]). This action moves the second layer
inside the first layer.

```javascript
var parLayer = fl.getDocumentDOM().getTimeline().layers[0];
parLayer.layerType = "folder";
fl.getDocumentDOM().getTimeline().layers[1].parentLayer = parLayer;
```