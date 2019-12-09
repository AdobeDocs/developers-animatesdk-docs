## TextureAtlasExporter.exportTextureAtlas()

#### Availability

Animate 2020.

#### Usage

TextureAtlasExporter.exportTextureAtlas(symbol, path)

#### Parameters

**_symbol_**:  Object;  The SymbolItem or SymbolInstance on which texture atlas should be generated.

#### Returns

Boolean.

#### Description

Method; Exports the texture atlas for the selected symbol.

#### Example

``` javascript
symbolsArr=fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements;

TextureAtlasExporter.exportTextureAtlas(symbolsArr[0].libraryItem)
````
