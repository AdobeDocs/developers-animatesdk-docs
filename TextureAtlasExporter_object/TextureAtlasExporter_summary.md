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
| [TextureAtlasExporter.exportTextureAtlas()](../TextureAtlasExporter_object/TextureAtlasExporter.md)| Exports the texture atlas for the selected symbol. |

#### Property summary

In addition to the Item object properties, the following properties are available for the SpriteSheetExporter object:

| **Property**                                       | **Description**                                                                                                          |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [TextureAtlasExporter.algorithm](../TextureAtlasExporter_object/TextureAtlasExporter1.md)     | Sets the encoding algorithm for the TextureAtlas                                |
| [TextureAtlasExporter.allowRotate](../TextureAtlasExporter_object/TextureAtlasExporter2.md)   | Allows sprites to be rotated when added to the TextureAtlas                                       
| [TextureAtlasExporter.app](../TextureAtlasExporter_object/TextureAtlasExporter3.md)           | A string indicating the name of the application that is generating the TextureAtlas.                                             |
| [TextureAtlasExporter.autoSize](../TextureAtlasExporter_object/TextureAtlasExporter4.md)      | A boolean value indicating whether the TextureAtlasExporter should calculate the overall size of TextureAtlas on its own.                                                                  |
| [TextureAtlasExporter.borderPadding](../TextureAtlasExporter_object/TextureAtlasExporter5.md) | An integer indicating the number of pixels of padding to add around each texture in the texture atlas.        
| [TextureAtlasExporter.canRotate](../TextureAtlasExporter_object/TextureAtlasExporter6.md)     | A boolean value indicating whether the framework specified by the TextureAtlasExporter.layoutFormat property may rotate textures when adding them to the texture atlas. |
| [TextureAtlasExporter.filePath](../TextureAtlasExporter_object/TextureAtlasExporter7.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.flattenSkewObject](../TextureAtlasExporter_object/TextureAtlasExporter8.md)   | It's the location where the texture atlas files needs to be exported.    |
| [TextureAtlasExporter.imageFormat](../TextureAtlasExporter_object/TextureAtlasExporter9.md)   | Boolean value which indicates whether skewed assets needs to be flattened to the texture atlas..    |
| [TextureAtlasExporter.optimizeBitmap](../TextureAtlasExporter_object/TextureAtlasExporter10.md)   | Boolean value which indicates whether texture atlas bitmaps needs to be optimized by removing extra spaces.    |
| [TextureAtlasExporter.optimizeJson](../TextureAtlasExporter_object/TextureAtlasExporter11.md)   |  Boolean value which indicates whether animation.json needs to be optimized by removing indentation, decomposed matrix and use shortened names.    |
| [TextureAtlasExporter.overflowed](../TextureAtlasExporter_object/TextureAtlasExporter12.md)   | Read-only property; Boolean value which indicates, if any assets are remaining after packing into texture atlas.    |
| [TextureAtlasExporter.resolution](../TextureAtlasExporter_object/TextureAtlasExporter13.md)   | Floating value which indicates in which resolution the textures needs to be exported.    |
| [TextureAtlasExporter.shapePadding](../TextureAtlasExporter_object/TextureAtlasExporter14.md)   | An integer value indicating how many pixels of padding should be added to each exported symbol frame when adding it to the TextureAtlas.    |
| [TextureAtlasExporter.sheetHeight](../TextureAtlasExporter_object/TextureAtlasExporter15.md)   | An integer value specifying the height of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true..    |
| [TextureAtlasExporter.sheetWidth](../TextureAtlasExporter_object/TextureAtlasExporter16.md)   | An integer value specifying the width of the texture atlas. This value is read-only if TextureAtlasExporter.autoSize is set to true.    |
| [TextureAtlasExporter.version](../TextureAtlasExporter_object/TextureAtlasExporter17.md)   | Read-only property; A stinrg indicating the version number of the Animate application. This property is provided for use by texture atlas plugins.    |