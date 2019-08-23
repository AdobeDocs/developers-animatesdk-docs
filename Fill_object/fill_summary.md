## fill summary

#### Availability

Flash MX 2004.

#### Description

This object contains all the properties of the Fill color setting of the Tools panel or of a selected shape. To retrieve a Fill object, use [document.getCustomFill()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume74.md).

#### Property summary

The following properties are available for the Fill object:

| **Property**                                                            | **Description**                                                                                                           |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [fill.bitmapIsClippe](#fill.bitmapIsClipped) [d](#fill.bitmapIsClipped) | A Boolean value that specifies whether the bitmap fill for a shape that is larger than the bitmap is clipped or repeated. |
| [fill.bitmapPath](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill1.md)                                        | A string that specifies the path and name of the bitmap fill in the Library.                                              |
| [fill.color](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill2.md)                                             | A string, hexadecimal value, or integer that represents the fill color.                                                   |
| [fill.colorArray](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill3.md)                                        | An array of colors in gradient.                                                                                           |
| [fill.focalPoint](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill4.md)                                        | An integer that specifies the gradient focal point horizontal offset from the transformation point.                       |
| [fill.linearRGB](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill5.md)                                         | A Boolean value that specifies whether to render the fill as a linear or radial RGB gradient.                             |
| [fill.matrix](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill6.md)                                            | A [Matrix object](#!AdobeDocs/developers-animatesdk-docs/test/Matrix_object/matrix_summary.md) that defines the placement, orientation, and scales for gradient fills.                  |
| [fill.overflow](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill7.md)                                          | A string that specifies the behavior of a gradient’s overflow.                                                            |
| [fill.posArray](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill8.md)                                          | An array of integers, each in the range of zero to 255, indicating the position of the corresponding color.               |
| [fill.style](#!AdobeDocs/developers-animatesdk-docs/test/Fill_object/fill9.md)                                             | A string that specifies the fill style.                                                                                   |

<span id="fill.bitmapIsClipped" class="anchor"></span>

