## stroke summary

#### Availability

Flash MX 2004.

#### Description

The Stroke object contains all the settings for a stroke, including the custom settings. This object represents the information contained in the Property inspector. Using the Stroke object together with the [document.setCustomStroke()](../Document_object/docum480.md) method, you can change the stroke settings for the Tools panel, the Property inspector, and the current selection. You can also get the stroke settings of the Tools panel and Property inspector, or of the current selection, by using the [document.getCustomStroke()](../Document_object/docume75.md) method.
This object always has the following four properties: style, thickness, color, and breakAtCorners. (In Flash CS3, the breakAtCorners property was deprecated in favor of [stroke.joinType](../Stroke_object/stroke11.md).) Other properties can be set, depending on the value of the [stroke.style](../Stroke_object/stroke20.md) property.

#### Property summary

The following properties are available for the Stroke object:

| **Property**                                    | **Description**                                                                                         |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [stroke.breakAtCorners](../Stroke_object/stroke.md) | A Boolean value, same as the Sharp Corners setting in the custom Stroke Style dialog box.               |
| [stroke.capType](../Stroke_object/stroke1.md)                 | A string that specifies the type of cap for the stroke.                                                 |
| [stroke.color](../Stroke_object/stroke2.md)                   | A string, hexadecimal value, or integer that represents the stroke color.                               |
| [stroke.curve](../Stroke_object/stroke3.md)                   | A string that specifies the type of hatching for the stroke.                                            |
| [stroke.dash1](../Stroke_object/stroke4.md)                   | An integer that specifies the lengths of the solid part of a dashed line.                               |
| [stroke.dash2](../Stroke_object/stroke5.md)                   | An integer that specifies the lengths of the blank part of a dashed line.                               |
| [stroke.density](../Stroke_object/stroke6.md)                 | A string that specifies the density of a stippled line.                                                 |
| [stroke.dotSize](../Stroke_object/stroke7.md)                 | A string that specifies the dot size of a stippled line.                                                |
| [stroke.dotSpace](../Stroke_object/stroke8.md)                | An integer that specifies the spacing between dots in a dotted line.                                    |
| [stroke.hatchThickness](../Stroke_object/stroke9.md)          | A string that specifies the thickness of a hatch line.                                                  |
| [stroke.jiggle](../Stroke_object/stroke10.md)                  | A string that specifies the jiggle property of a hatched line.                                          |
| [stroke.joinType](../Stroke_object/stroke11.md)                | A string that specifies the type of join for the stroke.                                                |
| [stroke.length](../Stroke_object/stroke12.md)                  | A string that specifies the length of a hatch line.                                                     |
| [stroke.miterLimit](../Stroke_object/stroke13.md)              | A float value that specifies the angle above which the tip of the miter will be truncated by a segment. |
| [stroke.pattern](../Stroke_object/stroke14.md)                 | A string that specifies the pattern of a ragged line.                                                   |
| [stroke.rotate](../Stroke_object/stroke15.md)                  | A string that specifies the rotation of a hatch line.                                                   |
| [stroke.scaleType](../Stroke_object/stroke16.md)               | A string that specifies the type of scale to be applied to the stroke.                                  |

| **Property**                          | **Description**                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------|
| [stroke.shapeFill](../Stroke_object/stroke17.md)     | A [Fill object](../Fill_object/fill_summary.md) that represents the fill settings of the stroke. |
| [stroke.space](../Stroke_object/stroke18.md)         | A string that specifies the spacing of a hatched line.                          |
| [stroke.strokeHinting](../Stroke_object/stroke19.md) | A Boolean value that specifies whether stroke hinting is set on the stroke.     |
| [stroke.style](../Stroke_object/stroke20.md)         | A string that describes the stroke style.                                       |
| [stroke.thickness](../Stroke_object/stroke21.md)     | An integer that specifies the stroke size.                                      |
| [stroke.variation](../Stroke_object/stroke22.md)     | A string that specifies the variation of a stippled line.                       |
| [stroke.waveHeight](../Stroke_object/stroke23.md)    | A string that specifies the wave height of a ragged line.                       |
| [stroke.waveLength](../Stroke_object/stroke24.md)    | A string that specifies the wave length of a ragged line.                       |

<span id="stroke.breakAtCorners" class="anchor"></span>

