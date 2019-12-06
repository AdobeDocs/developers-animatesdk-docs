## SpriteSheetExporter summary

**Inheritance** [Item object](../Item_object/item_summary.md) >SpriteSheetExporter object

#### Availability

Flash Pro CS6.

#### Description

The SpriteSheetExporter object is a subclass of the [Item object](../Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the SpriteSheetExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [SpriteSheetExporter.addBitmap()](../TextureAtlasExporter_object\TextureAtlasExporter.md) | Adds a bitmap or bitmapItem to the sprite sheet.      |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.algorithm](../SpriteSheetExporter_object/SpriteSheetExporte2.md)     | Sets the encoding algorithm for the sprite sheet.                                                                        |
| [SpriteSheetExporter.allowRotate](../SpriteSheetExporter_object/SpriteSheetExporte3.md)   | Allows sprites to be rotated when added to the sprite sheet.                                                             |
| [SpriteSheetExporter.allowTrimming](../SpriteSheetExporter_object/SpriteSheetExporte4.md) | Allows trimming of whitespace around sprites.                                                                            |
| [SpriteSheetExporter.app](../SpriteSheetExporter_object/SpriteSheetExporte5.md)           | A string indicating the name of the application generating the sprite sheet.                                             |
| [SpriteSheetExporter.autoSize](../SpriteSheetExporter_object/SpriteSheetExporte6.md)      | Automatically size the sprite sheet to fit all sprites.                                                                  |
| [SpriteSheetExporter.borderPadding](../SpriteSheetExporter_object/SpriteSheetExporte8.md) | The amount of padding around the sprite sheet borders, in pixels.                                                        |
| [SpriteSheetExporter.canBorderPad](../SpriteSheetExporter_object/SpriteSheetExporte9.md)  | A Boolean value indicating whether border padding is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.canRotate](../SpriteSheetExporter_object/SpriteSheetExport10.md)     | A Boolean value indicating whether sprite rotation is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canShapePad](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | A Boolean value indicating whether shape padding is supported by the framework specified by the layoutFormat property.   |

| **Property**                                                                       | **Description**                                                                                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.canStackDuplicateFrames](../SpriteSheetExporter_object/SpriteSheetExport13.md)     | A Boolean value indicating whether sprite stacking is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canTrim](../SpriteSheetExporter_object/SpriteSheetExport11.md)                                       | A Boolean value indicating whether shape trimming is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.format](../SpriteSheetExporter_object/SpriteSheetExport16.md)                                        | The format of the sprite sheet image file.                                                                               |
| [SpriteSheetExporter.image](../SpriteSheetExporter_object/SpriteSheetExport17.md)                                         | The name of the image file of the sprite sheet.                                                                          |
| [SpriteSheetExporter.layoutFormat](../SpriteSheetExporter_object/SpriteSheetExport18.md)                                  | The format of the sprite sheet metadata.                                                                                 |
| [SpriteSheetExporter.maxSheetHeight](../SpriteSheetExporter_object/SpriteSheetExport19.md) | Controls the maximum height of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.      |
| [SpriteSheetExporter.maxSheetWidth](../SpriteSheetExporter_object/SpriteSheetExport20.md)  | Controls the maximum width of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.       |
| [SpriteSheetExporter.overflowed](../SpriteSheetExporter_object/SpriteSheetExport21.md)                                    | A Boolean value indicating whether all the specified frames can fit in the specified sprite sheet size.                  |
| [SpriteSheetExporter.shapePadding](../SpriteSheetExporter_object/SpriteSheetExport24.md)                                  | The amount of padding around each sprite, in pixels.                                                                     |
| [SpriteSheetExporter.sheetHeight](../SpriteSheetExporter_object/SpriteSheetExport25.md)                                   | The height of the sprite sheet, in pixels.                                                                               |
| [SpriteSheetExporter.sheetWidth](../SpriteSheetExporter_object/SpriteSheetExport26.md)                                    | The width of the sprite sheet, in pixels.                                                                                |
| [SpriteSheetExporter.stackDuplicate](../SpriteSheetExporter_object/SpriteSheetExport27.md)        | A Boolean value indicating whether to stack identical symbol frames in the sprite sheet.                                 |
| [SpriteSheetExporter.version](../SpriteSheetExporter_object/SpriteSheetExport28.md)                                       | The version number of the application creating the sprite sheet.                                                         |

<span id="SpriteSheetExporter.addBitmap()" class="anchor"></span>

