## SpriteSheetExporter.format

#### Availability

Flash Pro CS6.

#### Usage

SpriteSheetExporter.format

#### Description

Read-only property; A string value indicating the format of the sprite sheet image file. Possible values include “RGBA8888”, “RGB888x”, and “RGB8”. This property is provided for use by sprite sheet generator plugins.

#### Example

```
var exporter = new SpriteSheetExporter; alert(exporter.format);
// "RGBA8888"

```