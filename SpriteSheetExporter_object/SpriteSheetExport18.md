## SpriteSheetExporter.layoutFormat

#### Availability

Flash Pro CS6.

#### Usage

SpriteSheetExporter.layoutFormat

#### Description

Property; A string value indicating the format of the sprite sheet metadata. Valid values depend on the contents of the Sprite Sheet Plugin directory. “JSON” (JavaScript Object Notation) is one possible value. Your script passes the layout format’s ID string to match one of the .jsfl files defined for the Sprite Sheet plugin (located in the *flashroot*/Common/Configuration/Sprite Sheet Plugins folder). These files have the naming convention *layoutformat*.plugin.jsfl and you pass a string set to *layoutformat*. For example, you would set layoutFormat equal to "Starling", "cocos2D v2", or "cocos2D v3".

#### Example

```
var exporter = new SpriteSheetExporter; exporter.layoutFormat = "JSON";

```