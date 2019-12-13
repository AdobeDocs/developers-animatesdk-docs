## layer summary

#### Availability

Flash MX 2004.

#### Description

The Layer object represents a layer in the timeline. The [timeline.layers](../Timeline_object/timeli31.md) property contains an array of Layer objects, which can be accessed by fl.getDocumentDOM().getTimeline().layers.

#### Method summary

The following methods are available for the Item object:

| **Method**                             | **Description**                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [layer.getBlendModeAtFrame()](../Item_object/item.md)      | A string value that specifies the blend mode at frame.                                                                                         |
| [layer.getColorTransformAtFrame()](../Item_object/item1.md)        | Based on the mode, the paramters will be updated here. For example, if tint is present, the value corresponding to tint only will be present along with the color matrix values..                                                                                     |
| [layer.getFiltersAtFrame()](../Item_object/item.md)      | An array that contains a list of filters applied to the frame at frameIndex.                                                                                         |
| [layer.getZDepthAtFrame()	](../Item_object/item.md)      | An integer value that specifies the ZDepth valur at the frame.                                                                                         |
| [layer.setBlendModeAtFrame()](../Item_object/item.md)      |FrameNumber :frame index,  ZVal:int.                                                                                         |
| [layer.setColorTransformAtFrame()](../Item_object/item.md)      | frameIndex – int, cxFormObject - The cxform to be set	.                                                                                         |
| [layer. setFiltersAtFrame()](../Item_object/item.md)      | frameIndex – int, filterArray - The array of filters to be set.                                                                                         |
| [layer.setZDepthAtFrame()	](../Item_object/item1.md)        | Enables to set ZDepth value at the frame.                                                                                     |

#### Property summary

The following properties are available for the Layer object:

| **Property**                                                         | **Description**                                                                                                                 |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [layer.animationType](../Layer_object/layer.md)| The layer type: "none", "motion object", or "IK pose".                                                                          |
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

