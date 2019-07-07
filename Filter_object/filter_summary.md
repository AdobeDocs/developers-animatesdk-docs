## filter summary

#### Availability

Flash 8.

#### Description

This object contains all the properties for all filters. The filter.name property specifies the type of filter, and determines which properties are applicable to each filter. See [filter.name](#_bookmark440).
To return the filter list for an object or objects, use document.getFilters(). To apply filters to an object or objects, use document.setFilters(). See [document.getFilters()](#_bookmark208) and [document.setFilters()](#_bookmark291).

#### Property summary

The following properties can be used with the Filter object:

| **Property**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [filter.angle](#filter.angle)          | A float value that specifies the angle of the shadow or highlight color, in degrees.            |
| [filter.blurX](#_bookmark428)          | A float value that specifies the amount to blur in the x direction, in pixels.                  |
| [filter.blurY](#_bookmark429)          | A float value that specifies the amount to blur in the y direction.                             |
| [filter.brightness](#_bookmark430)     | A float value that specifies the brightness of the filter.                                      |
| [filter.color](#_bookmark431)          | A string, hexadecimal value, or integer that represents the filter color.                       |
| [filter.contrast](#_bookmark432)       | A float value that specifies the contrast value of the filter.                                  |
| [filter.distance](#_bookmark433)       | A float value that specifies the distance between the filter’s effect and an object, in pixels. |
| [filter.enabled](#_bookmark434)        | A Boolean value that specifies whether the specified filter is enabled.                         |
| [filter.hideObject](#_bookmark435)     | A Boolean value that specifies whether the source image is hidden.                              |
| [filter.highlightColor](#_bookmark436) | A string, hexadecimal value, or integer that represents the highlight color.                    |
| [filter.hue](#_bookmark437)            | A float value that specifies the hue of the filter.                                             |
| [filter.inner](#_bookmark438)          | A Boolean value that specifies whether the shadow is an inner shadow.                           |
| [filter.knockout](#_bookmark439)       | A Boolean value that specifies whether the filter is a knockout filter.                         |
| [filter.name](#_bookmark440)           | Read-only; a string that specifies the type of filter.                                          |
| [filter.quality](#_bookmark441)        | A string that specifies the blur quality.                                                       |
| [filter.saturation](#_bookmark442)     | A float value that specifies the saturation value of the filter.                                |
| [filter.shadowColor](#_bookmark443)    | A string, hexadecimal value, or integer that represents the shadow color.                       |
| [filter.strength](#_bookmark444)       | An integer that specifies the percentage strength of the filter.                                |
| [filter.type](#_bookmark445)           | A string that specifies the type of bevel or glow.                                              |

<span id="filter.angle" class="anchor"></span>

