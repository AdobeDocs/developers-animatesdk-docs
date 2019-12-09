## TextureAtlasExporter.imageFormat

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.imageFormat

#### Description

Property;String or Object. A string or an object that describes the type of image format to generate.
• String: Valid values are either "png" or "jpg", the exporter use whatever values where last used.
• Object: If you pass an object, it needs at least a string property "format" which is either "png" or "jpg". Optionally
the object may include "backgroundColor," which is a valid color value (alpha may be included); "quality" (jpg
only), which is an integer from 1 to 100; and "bitDepth" (png only) which can be 8, 24 or 32..

#### Example

``` java script

````