## TextureAtlasExporter.canRotate

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.canRotate

#### Description

Read-only property; A boolean value indicating whether the framework specified by the
TextureAtlasExporter.layoutFormat property may rotate textures when adding them to the texture atlas.

#### Example

``` javascript
var exporter = new TextureAtlasExporter;
alert(exporter.canRotate);
````