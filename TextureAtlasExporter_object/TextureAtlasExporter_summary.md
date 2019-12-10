## TextureAtlasExporter summary

**Inheritance** [Item object](../Item_object/item_summary.md) >TextureAtlasExporter object

#### Availability

Animate 2020.

#### Description

The TextureAtlasExporter object is a subclass of the [Item object](../Item_object/item_summary.md).

#### Method summary

In addition to the Item object methods, you can use the following methods with the TextureAtlasExporter object:

| **Method**                                                          | **Description**                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------|
| [TextureAtlasExporter.exportTextureAtlas()](../TextureAtlasExporter_object\TextureAtlasExporter.md)| Exports the texture atlas for the selected symbol. |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [TextureAtlasExporter.algorithm](../SpriteSheetExporter_object/SpriteSheetExporte2.md)     | Sets the encoding algorithm for the TextureAtlas                                |
| [TextureAtlasExporter.allowRotate](../SpriteSheetExporter_object/SpriteSheetExporte3.md)   | Allows sprites to be rotated when added to the TextureAtlas                                       
| [TextureAtlasExporter.app](../SpriteSheetExporter_object/SpriteSheetExporte5.md)           | A string indicating the name of the application that is generating the TextureAtlas.                                             |
| [TextureAtlasExporter.autoSize](../SpriteSheetExporter_object/SpriteSheetExporte6.md)      | A boolean value indicating whether the TextureAtlasExporter should calculate the overall size of TextureAtlas on its own.                                                                  |
| [TextureAtlasExporter.borderPadding](../SpriteSheetExporter_object/SpriteSheetExporte8.md) | An integer indicating the number of pixels of padding to add around each texture in the texture atlas.        
| [TextureAtlasExporter.canRotate](../SpriteSheetExporter_object/SpriteSheetExport10.md)     | A boolean value indicating whether the framework specified by the TextureAtlasExporter.layoutFormat property may rotate textures when adding them to the texture atlas. |
| [TextureAtlasExporter.filePath](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.flattenSkewObject](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.imageFormat](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | Boolean value which indicates whether skewed assets needs to be flattened to the texture atlas..    |
| [TextureAtlasExporter.optimizeBitmap](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | Boolean value which indicates whether texture atlas bitmaps needs to be optimized by removing extra spaces.    |
| [TextureAtlasExporter.optimizeJson](../SpriteSheetExporter_object/SpriteSheetExport12.md)   |  Boolean value which indicates whether animation.json needs to be optimized by removing indentation, decomposed matrix and use shortened names.    |
| [TextureAtlasExporter.overflowed](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | Read-only property; Boolean value which indicates, if any assets are remaining after packing into texture atlas.    |
| [TextureAtlasExporter.resolution](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | Floating value which indicates in which resolution the textures needs to be exported.    |
| [TextureAtlasExporter.shapePadding](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | An integer value indicating how many pixels of padding should be added to each exported symbol frame when adding it to the TextureAtlas.    |
| [TextureAtlasExporter.sheetHeight](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | An integer value specifying the height of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true..    |
| [TextureAtlasExporter.sheetWidth](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | An integer value specifying the width of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true.    |
| [TextureAtlasExporter.version](../SpriteSheetExporter_object/SpriteSheetExport12.md)   | Read-only property; A stinrg indicating the version number of the Animate application. This property is provided for use by texture atlas plugins.    |