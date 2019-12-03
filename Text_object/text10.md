## text.fontRenderingMode

#### Availability

Flash 8.

#### Usage

text.fontRenderingMode

#### Description

Property; a string that specifies the rendering mode for the text. This property affects how the text is displayed both on the Stage and in Flash Player. Acceptable values are described in the following table:

| **Property value** | **How text is rendered**                                    |
|--------------------|-------------------------------------------------------------|
| device             | Renders the text with device fonts.                         |
| bitmap             | Renders aliased text as a bitmap, or as a pixel font would. |



| **Property value**       | **How text is rendered**                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| standard                 | Renders text using the standard anti-aliasing method used by Flash MX 2004. This is the best setting to use for animated, very large, or skewed text.                                    |
| advanced                 | Renders text using the advanced anti-aliasing font rendering technology implemented in Flash 8, which produces better anti-aliasing and improves readability, especially for small text. |
| customThicknessSharpness | Lets you specify custom settings for the sharpness and thickness of the text when using the advanced anti-aliasing font rendering technology implemented in Flash 8.                     |

#### Example

The following example shows how you can use the customThicknessSharpness value to specify the sharpness and thickness of the text:
```javascript
fl.getDocumentDOM().setElementProperty("fontRenderingMode", "customThicknessSharpness"); fl.getDocumentDOM().setElementProperty("antiAliasSharpness", 400);
fl.getDocumentDOM().setElementProperty("antiAliasThickness", -200);
```
#### See also

[text.antiAliasSharpness](../Text_object/text1.md), [text.antiAliasThickness](../Text_object/text2.md)
