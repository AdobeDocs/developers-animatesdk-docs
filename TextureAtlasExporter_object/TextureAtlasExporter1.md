## TextureAtlasExporter.algorithm

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.algorithm

#### Description

Property;  A string indicating which algorithm to use to pack the TextureAtlas. Valid values are "basic", and
"maxRects" (the default).

#### Example

``` javascript
var exporter = new TextureAtlasExporter;
exporter.algorithm = "maxRects";
````