## text.embedVariantGlyphs

#### Availability

> Flash CS4 Professional.

#### Usage

> text.embedVariantGlyphs

#### Description

> Property; a Boolean value that specifies whether to enable the embedding of variant glyphs (true) or not (false). This property works only with dynamic or input text; it is ignored if used with static text. The default value is false.
>
> ***Note:** Beginning in Flash Professional CS5, font embedding is controlled at the document level instead of the text object level. Use the* *[“fontItem.embedVariantGlyphs” on page 311](#_bookmark589) property instead of the text.embedVariantGlyphs property. In Flash Professional CS5, the text.embedVariantGlyphs property no longer has any effect because Flash always embeds variant glyphs for TLF text and never embeds them for Classic text.*

#### Example

> The following example enables variant glyphs to be embedded in the selected Text object:
>
> fl.getDocumentDOM().selection\[0\].embedVariantGlyphs = true;

#### See also

> [fontItem.embedVariantGlyphs](#_bookmark589)
