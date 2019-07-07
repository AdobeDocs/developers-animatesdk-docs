## fill summary

#### Availability

Flash MX 2004.

#### Description

This object contains all the properties of the Fill color setting of the Tools panel or of a selected shape. To retrieve a Fill object, use [document.getCustomFill()](#_bookmark201).

#### Property summary

The following properties are available for the Fill object:

| **Property**                                                            | **Description**                                                                                                           |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [fill.bitmapIsClippe](#fill.bitmapIsClipped) [d](#fill.bitmapIsClipped) | A Boolean value that specifies whether the bitmap fill for a shape that is larger than the bitmap is clipped or repeated. |
| [fill.bitmapPath](#_bookmark415)                                        | A string that specifies the path and name of the bitmap fill in the Library.                                              |
| [fill.color](#_bookmark416)                                             | A string, hexadecimal value, or integer that represents the fill color.                                                   |
| [fill.colorArray](#_bookmark417)                                        | An array of colors in gradient.                                                                                           |
| [fill.focalPoint](#_bookmark418)                                        | An integer that specifies the gradient focal point horizontal offset from the transformation point.                       |
| [fill.linearRGB](#_bookmark419)                                         | A Boolean value that specifies whether to render the fill as a linear or radial RGB gradient.                             |
| [fill.matrix](#_bookmark420)                                            | A [Matrix object](#_bookmark725) that defines the placement, orientation, and scales for gradient fills.                  |
| [fill.overflow](#_bookmark421)                                          | A string that specifies the behavior of a gradient’s overflow.                                                            |
| [fill.posArray](#_bookmark422)                                          | An array of integers, each in the range of zero to 255, indicating the position of the corresponding color.               |
| [fill.style](#_bookmark423)                                             | A string that specifies the fill style.                                                                                   |

<span id="fill.bitmapIsClipped" class="anchor"></span>

