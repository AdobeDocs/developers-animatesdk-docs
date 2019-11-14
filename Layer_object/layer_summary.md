## layer summary

#### Availability

Flash MX 2004.

#### Description

The Layer object represents a layer in the timeline. The [timeline.layers](../Timeline_object/timeli31.md) property contains an array of Layer objects, which can be accessed by fl.getDocumentDOM().getTimeline().layers.

#### Property summary

The following properties are available for the Layer object:

| **Property**                                                         | **Description**                                                                                                                 |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [layer.animationTyp](#layer.animationType) [e](#layer.animationType) | The layer type: "none", "motion object", or "IK pose".                                                                          |
| [layer.color](../Layer_object/layer1.md)                                         | A string, hexadecimal value, or integer that specifies the color assigned to outline the layer.                                 |
| [layer.frameCount](../Layer_object/layer2.md)                                    | Read-only; an integer that specifies the number of frames in the layer.                                                         |
| [layer.frames](../Layer_object/layer3.md)                                        | Read-only; an array of Frame objects.                                                                                           |
| [layer.height](../Layer_object/layer4.md)                                        | An integer that specifies the percentage layer height; equivalent to the Layer height value in the Layer Properties dialog box. |
| [layer.layerType](../Layer_object/layer5.md)                                     | A string that specifies the current use of the layer; equivalent to the Type setting in the Layer Properties dialog box.        |
| [layer.locked](../Layer_object/layer6.md)                                        | A Boolean value that specifies the locked status of the layer.                                                                  |
| [layer.name](../Layer_object/layer7.md)                                          | A string that specifies the name of the layer.                                                                                  |
| [layer.outline](../Layer_object/layer8.md)                                       | A Boolean value that specifies the status of outlines for all objects in the layer.                                             |
| [layer.parentLayer](../Layer_object/layer9.md)                                   | A Layer object that represents the layer’s containing folder, guiding, or masking layer.                                        |
| [layer.visible](../Layer_object/layer10.md)                                       | A Boolean value that specifies whether the layer’s objects on the Stage are shown or hidden.                                    |

<span id="layer.animationType" class="anchor"></span>

