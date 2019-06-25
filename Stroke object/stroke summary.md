## stroke summary

#### Availability

> Flash MX 2004.

#### Description

> The Stroke object contains all the settings for a stroke, including the custom settings. This object represents the information contained in the Property inspector. Using the Stroke object together with the [document.setCustomStroke()](#_bookmark282) method, you can change the stroke settings for the Tools panel, the Property inspector, and the current selection. You can also get the stroke settings of the Tools panel and Property inspector, or of the current selection, by using the [document.getCustomStroke()](#_bookmark203) method.
>
> This object always has the following four properties: style, thickness, color, and breakAtCorners. (In Flash CS3, the breakAtCorners property was deprecated in favor of [stroke.joinType](#_bookmark889).) Other properties can be set, depending on the value of the [stroke.style](#_bookmark898) property.

#### Property summary

> The following properties are available for the Stroke object:

| **Property**                                    | **Description**                                                                                         |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [stroke.breakAtCorners](#stroke.breakAtCorners) | A Boolean value, same as the Sharp Corners setting in the custom Stroke Style dialog box.               |
| [stroke.capType](#_bookmark879)                 | A string that specifies the type of cap for the stroke.                                                 |
| [stroke.color](#_bookmark880)                   | A string, hexadecimal value, or integer that represents the stroke color.                               |
| [stroke.curve](#_bookmark881)                   | A string that specifies the type of hatching for the stroke.                                            |
| [stroke.dash1](#_bookmark882)                   | An integer that specifies the lengths of the solid part of a dashed line.                               |
| [stroke.dash2](#_bookmark883)                   | An integer that specifies the lengths of the blank part of a dashed line.                               |
| [stroke.density](#_bookmark884)                 | A string that specifies the density of a stippled line.                                                 |
| [stroke.dotSize](#_bookmark885)                 | A string that specifies the dot size of a stippled line.                                                |
| [stroke.dotSpace](#_bookmark886)                | An integer that specifies the spacing between dots in a dotted line.                                    |
| [stroke.hatchThickness](#_bookmark887)          | A string that specifies the thickness of a hatch line.                                                  |
| [stroke.jiggle](#_bookmark888)                  | A string that specifies the jiggle property of a hatched line.                                          |
| [stroke.joinType](#_bookmark889)                | A string that specifies the type of join for the stroke.                                                |
| [stroke.length](#_bookmark890)                  | A string that specifies the length of a hatch line.                                                     |
| [stroke.miterLimit](#_bookmark891)              | A float value that specifies the angle above which the tip of the miter will be truncated by a segment. |
| [stroke.pattern](#_bookmark892)                 | A string that specifies the pattern of a ragged line.                                                   |
| [stroke.rotate](#_bookmark893)                  | A string that specifies the rotation of a hatch line.                                                   |
| [stroke.scaleType](#_bookmark894)               | A string that specifies the type of scale to be applied to the stroke.                                  |

| **Property**                          | **Description**                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------|
| [stroke.shapeFill](#_bookmark895)     | A [Fill object](#_bookmark412) that represents the fill settings of the stroke. |
| [stroke.space](#_bookmark896)         | A string that specifies the spacing of a hatched line.                          |
| [stroke.strokeHinting](#_bookmark897) | A Boolean value that specifies whether stroke hinting is set on the stroke.     |
| [stroke.style](#_bookmark898)         | A string that describes the stroke style.                                       |
| [stroke.thickness](#_bookmark899)     | An integer that specifies the stroke size.                                      |
| [stroke.variation](#_bookmark900)     | A string that specifies the variation of a stippled line.                       |
| [stroke.waveHeight](#_bookmark901)    | A string that specifies the wave height of a ragged line.                       |
| [stroke.waveLength](#_bookmark902)    | A string that specifies the wave length of a ragged line.                       |

<span id="stroke.breakAtCorners" class="anchor"></span>
