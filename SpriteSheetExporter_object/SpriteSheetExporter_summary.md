## SpriteSheetExporter summary

**Inheritance** [Item object](#_bookmark658) \SpriteSheetExporter object

#### Availability

Flash Pro CS6.

#### Description

The SpriteSheetExporter object is a subclass of the [Item object](#_bookmark658).

#### Method summary

In addition to the Item object methods, you can use the following methods with the SpriteSheetExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [SpriteSheetExporter.addBitmap()](#SpriteSheetExporter.addBitmap()) | Adds a bitmap or bitmapItem to the sprite sheet.                  |
| [SpriteSheetExporter.addSymbol()](#_bookmark847)                    | Adds a symbol to be used to generate the sprite sheet.            |
| [SpriteSheetExporter.beginExport()](#_bookmark853)                  | Initializes the SpriteSheetExporter to create a new sprite sheet. |
| [SpriteSheetExporter.changeSymbol()](#_bookmark860)                 | Changes which symbol frames will be added to the sprite sheet.    |
| [SpriteSheetExporter.exportSpriteSheet()](#_bookmark861)            | Export the sprite sheet into a an image file.                     |
| [SpriteSheetExporter.removeBitmap()](#_bookmark868)                 | Remove a bitmap object from the sprite sheet.                     |
| [SpriteSheetExporter.removeSymbol()](#_bookmark869)                 | Remove a symbol from the sprite sheet.                            |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.algorithm](#_bookmark848)     | Sets the encoding algorithm for the sprite sheet.                                                                        |
| [SpriteSheetExporter.allowRotate](#_bookmark849)   | Allows sprites to be rotated when added to the sprite sheet.                                                             |
| [SpriteSheetExporter.allowTrimming](#_bookmark850) | Allows trimming of whitespace around sprites.                                                                            |
| [SpriteSheetExporter.app](#_bookmark851)           | A string indicating the name of the application generating the sprite sheet.                                             |
| [SpriteSheetExporter.autoSize](#_bookmark852)      | Automatically size the sprite sheet to fit all sprites.                                                                  |
| [SpriteSheetExporter.borderPadding](#_bookmark854) | The amount of padding around the sprite sheet borders, in pixels.                                                        |
| [SpriteSheetExporter.canBorderPad](#_bookmark855)  | A Boolean value indicating whether border padding is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.canRotate](#_bookmark856)     | A Boolean value indicating whether sprite rotation is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canShapePad](#_bookmark858)   | A Boolean value indicating whether shape padding is supported by the framework specified by the layoutFormat property.   |

| **Property**                                                                       | **Description**                                                                                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SpriteSheetExporter.canStackDuplic](#_bookmark859) [ateFrames](#_bookmark859)     | A Boolean value indicating whether sprite stacking is supported by the framework specified by the layoutFormat property. |
| [SpriteSheetExporter.canTrim](#_bookmark857)                                       | A Boolean value indicating whether shape trimming is supported by the framework specified by the layoutFormat property.  |
| [SpriteSheetExporter.format](#_bookmark862)                                        | The format of the sprite sheet image file.                                                                               |
| [SpriteSheetExporter.image](#_bookmark863)                                         | The name of the image file of the sprite sheet.                                                                          |
| [SpriteSheetExporter.layoutFormat](#_bookmark864)                                  | The format of the sprite sheet metadata.                                                                                 |
| [“SpriteSheetExporter.maxSheetHeight” on](#_bookmark865) [page 442](#_bookmark865) | Controls the maximum height of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.      |
| [“SpriteSheetExporter.maxSheetWidth”](#_bookmark866) [on page 442](#_bookmark866)  | Controls the maximum width of the generated sprite sheet when autoSize = true, clipped to a maximum value of 8192.       |
| [SpriteSheetExporter.overflowed](#_bookmark867)                                    | A Boolean value indicating whether all the specified frames can fit in the specified sprite sheet size.                  |
| [SpriteSheetExporter.shapePadding](#_bookmark870)                                  | The amount of padding around each sprite, in pixels.                                                                     |
| [SpriteSheetExporter.sheetHeight](#_bookmark871)                                   | The height of the sprite sheet, in pixels.                                                                               |
| [SpriteSheetExporter.sheetWidth](#_bookmark872)                                    | The width of the sprite sheet, in pixels.                                                                                |
| [SpriteSheetExporter.stackDuplicate](#_bookmark873) [Frames](#_bookmark873)        | A Boolean value indicating whether to stack identical symbol frames in the sprite sheet.                                 |
| [SpriteSheetExporter.version](#_bookmark874)                                       | The version number of the application creating the sprite sheet.                                                         |

<span id="SpriteSheetExporter.addBitmap()" class="anchor"></span>

