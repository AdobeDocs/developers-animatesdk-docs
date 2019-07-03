## fontItem.embedVariantGlyphs

#### Availability

Flash CS4 Professional.

#### Usage

fontItem.embedVariantGlyphs

#### Description

***Note:** While this property is available in Flash CS5 Professional, it has no effect when applied to Text Layout Framework (TLF) text. Beginning in Flash Professional CS5, variant glyphs are always embedded in fonts used with TLF text. The flash.text.engine (FTE) referenced below is only available in Flash Professional CS4.*
Property; a Boolean value that specifies whether variant glyphs should be output in the font when publishing a SWF file (true) or not (false). Setting this value to true increases the size of your SWF file. The default value is false.
Some languages dynamically substitute characters glyphs as you are typing (for example, Thai, Arabic, Hebrew, and Greek). If you are laying out or inputting text in these types of languages, set this property to true.

#### Examples

```
Font symbols that are compatible with flash.text APIs appear in the Library and the user can manage them directly. However, font symbols that are compatible with the flash.text.engine (FTE) APIs do not appear in the Library, so you must manage them manually. The following function adds a new font to the Library that can be used with the FTE APIs.
function embedFontSymbol(symbolName, fontName, includeVariants) { var doc = fl.getDocumentDOM();
if (doc) {
// look up the item. if it exists, delete it.
var index = doc.library.findItemIndex(symbolName); if (index \-1)
doc.library.deleteItem(symbolName);
// make a new font symbol in the library doc.library.addNewItem('font', symbolName);
// look up the symbol by its name
var index = doc.library.findItemIndex(symbolName); if (index \-1) {
// get the item from the library and set the attributes of interest var fontObj = doc.library.items\[index\];
fontObj.isDefineFont4Symbol = true; fontObj.font = fontName; fontObj.bold = false; fontObj.italic = false;
fontObj.embedVariantGlyphs = includeVariants;
// this is what forces the font into the SWF stream fontObj.linkageExportForAS = true; fontObj.linkageExportInFirstFrame = true;
}
}
}
The following function displays all the font symbols in the Output panel.
function dumpFontSymbols()
{
var doc = fl.getDocumentDOM(); if (doc) {
var items = doc.library.items; fl.trace("items length = " + items.length); var i;
for(i=0; i\<items.length; i++) { var item = items\[i\];
fl.trace("itemType = " + item.itemType); if (item.itemType == 'font') {
fl.trace("name = " + item.name);
fl.trace("DF4 symbol = " + item.isDefineFont4Symbol); fl.trace("font = " + item.font);
}
}
}
}

```
#### See also

[fontItem.isDefineFont4Symbol](#_bookmark591), [text.embedVariantGlyphs](#_bookmark978)
