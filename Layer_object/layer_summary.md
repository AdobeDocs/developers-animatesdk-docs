## layer summary

#### Availability

Flash MX 2004.

#### Description

The Layer object represents a layer in the timeline. The [timeline.layers](#_bookmark1066) property contains an array of Layer objects, which can be accessed by fl.getDocumentDOM().getTimeline().layers.

#### Property summary

The following properties are available for the Layer object:

| **Property**                                                         | **Description**                                                                                                                 |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [layer.animationTyp](#layer.animationType) [e](#layer.animationType) | The layer type: "none", "motion object", or "IK pose".                                                                          |
| [layer.color](#_bookmark682)                                         | A string, hexadecimal value, or integer that specifies the color assigned to outline the layer.                                 |
| [layer.frameCount](#_bookmark683)                                    | Read-only; an integer that specifies the number of frames in the layer.                                                         |
| [layer.frames](#_bookmark684)                                        | Read-only; an array of Frame objects.                                                                                           |
| [layer.height](#_bookmark685)                                        | An integer that specifies the percentage layer height; equivalent to the Layer height value in the Layer Properties dialog box. |
| [layer.layerType](#_bookmark686)                                     | A string that specifies the current use of the layer; equivalent to the Type setting in the Layer Properties dialog box.        |
| [layer.locked](#_bookmark687)                                        | A Boolean value that specifies the locked status of the layer.                                                                  |
| [layer.name](#_bookmark688)                                          | A string that specifies the name of the layer.                                                                                  |
| [layer.outline](#_bookmark689)                                       | A Boolean value that specifies the status of outlines for all objects in the layer.                                             |
| [layer.parentLayer](#_bookmark690)                                   | A Layer object that represents the layer’s containing folder, guiding, or masking layer.                                        |
| [layer.visible](#_bookmark691)                                       | A Boolean value that specifies whether the layer’s objects on the Stage are shown or hidden.                                    |

<span id="layer.animationType" class="anchor"></span>

