## SpriteSheetExporter summary

**Inheritance** [Item object](#!AdobeDocs/developers-animatesdk-docs/test/Item_object/item_summary.md) \SpriteSheetExporter object

#### Availability

Flash Pro CS6.

#### Description

The SpriteSheetExporter object is a subclass of the [Item object](#!AdobeDocs/developers-animatesdk-docs/test/Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the SpriteSheetExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [SpriteSheetExporter.addBitmap()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporter.md)) | Adds a bitmap or bitmapItem to the sprite sheet.                  |
| [SpriteSheetExporter.addSymbol()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte1.md)                    | Adds a symbol to be used to generate the sprite sheet.            |
| [SpriteSheetExporter.beginExport()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte7.md)                  | Initializes the SpriteSheetExporter to create a new sprite sheet. |
| [SpriteSheetExporter.changeSymbol()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport14.md)                 | Changes which symbol frames will be added to the sprite sheet.    |
| [SpriteSheetExporter.exportSpriteSheet()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport15.md)            | Export the sprite sheet into a an image file.                     |
| [SpriteSheetExporter.removeBitmap()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport22.md)                 | Remove a bitmap object from the sprite sheet.                     |
| [SpriteSheetExporter.removeSymbol()](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport23.md)                 | Remove a symbol from the sprite sheet.                            |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.algorithm](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte2.md)     | Sets the encoding algorithm for the sprite sheet.                                                                        |
| [SpriteSheetExporter.allowRotate](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte3.md)   | Allows sprites to be rotated when added to the sprite sheet.                                                             |
| [SpriteSheetExporter.allowTrimming](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte4.md) | Allows trimming of whitespace around sprites.                                                                            |
| [SpriteSheetExporter.app](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte5.md)           | A string indicating the name of the application generating the sprite sheet.                                             |
| [SpriteSheetExporter.autoSize](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte6.md)      | Automatically size the sprite sheet to fit all sprites.                                                                  |
| [SpriteSheetExporter.borderPadding](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte8.md) | The amount of padding around the sprite sheet borders, in pixels.                                                        |
| [SpriteSheetExporter.canBorderPad](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExporte9.md)  | A Boolean value indicating whether border padding is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.canRotate](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport10.md)     | A Boolean value indicating whether sprite rotation is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canShapePad](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport12.md)   | A Boolean value indicating whether shape padding is supported by the framework specified by the layoutFormat property.   |

| **Property**                                                                       | **Description**                                                                                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.canStackDuplic](#_bookmark859) [ateFrames](#_bookmark859)     | A Boolean value indicating whether sprite stacking is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canTrim](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport11.md)                                       | A Boolean value indicating whether shape trimming is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.format](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport16.md)                                        | The format of the sprite sheet image file.                                                                               |
| [SpriteSheetExporter.image](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport17.md)                                         | The name of the image file of the sprite sheet.                                                                          |
| [SpriteSheetExporter.layoutFormat](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport18.md)                                  | The format of the sprite sheet metadata.                                                                                 |
| ["SpriteSheetExporter.maxSheetHeight" on](#_bookmark865) [page 442](#_bookmark865) | Controls the maximum height of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.      |
| ["SpriteSheetExporter.maxSheetWidth"](#_bookmark866) [on page 442](#_bookmark866)  | Controls the maximum width of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.       |
| [SpriteSheetExporter.overflowed](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport21.md)                                    | A Boolean value indicating whether all the specified frames can fit in the specified sprite sheet size.                  |
| [SpriteSheetExporter.shapePadding](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport24.md)                                  | The amount of padding around each sprite, in pixels.                                                                     |
| [SpriteSheetExporter.sheetHeight](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport25.md)                                   | The height of the sprite sheet, in pixels.                                                                               |
| [SpriteSheetExporter.sheetWidth](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport26.md)                                    | The width of the sprite sheet, in pixels.                                                                                |
| [SpriteSheetExporter.stackDuplicate](#_bookmark873) [Frames](#_bookmark873)        | A Boolean value indicating whether to stack identical symbol frames in the sprite sheet.                                 |
| [SpriteSheetExporter.version](#!AdobeDocs/developers-animatesdk-docs/test/SpriteSheetExporter_object/SpriteSheetExport28.md)                                       | The version number of the application creating the sprite sheet.                                                         |

<span id="SpriteSheetExporter.addBitmap()" class="anchor"></span>

