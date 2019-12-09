## TextureAtlasExporter.canRotate

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.canRotate

#### Description

Read-only property; A boolean value indicating whether the framework specified by the
SpriteSheetExporter.layoutFormat property may rotate symbol frames when adding them to the sprite sheet.

#### Example

``` java script
var exporter = new TextureAtlasExporter;
alert(exporter.canRotate);
````