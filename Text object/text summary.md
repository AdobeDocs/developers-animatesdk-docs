## text summary

> **Inheritance** [Element object](#_bookmark374) \> Text object

#### Availability

> Flash MX 2004.

#### Description

> The Text object represents a single text item in a document. All properties of the text pertain to the entire text block.
>
> To set properties of a text run within the text field, see the Property summary for the [TextAttrs object](#_bookmark1003). To change properties of a selection within a text field, you can use [document.setElementTextAttr()](#_bookmark286) and specify a range of text, or use the current selection.
>
> To set generic properties of the selected text field, use [document.setElementProperty()](#_bookmark284). The following example sets the x value of the selected text field's registration point to 50:
>
> fl.getDocumentDOM().setElementProperty("x", 50);

#### Method summary

> In addition to the Element object methods, the following methods are available for the Text object:

| **Method**                            | **Description**                                                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [text.getTextAttr()](#_bookmark981)   | Retrieves the specified attribute for the text identified by the optional ***startIndex*** and ***endIndex*** parameters. |
| [text.getTextString()](#_bookmark982) | Retrieves the specified range of text.                                                                                    |
| [text.setTextAttr()](#_bookmark992)   | Sets the specified attribute associated with the text identified by ***startIndex*** and ***endIndex***.                  |
| [text.setTextString()](#_bookmark993) | Changes the text string within this Text object.                                                                          |

#### Property summary

> In addition to the Element object properties, the following properties are available for the Text object:

| **Property**                             | **Description**                                                                                                                                      |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [text.accName](#text.accName)            | A string that is equivalent to the Name field in the Accessibility panel.                                                                            |
| [text.antiAliasSharpness](#_bookmark970) | A float value that specifies the anti-aliasing sharpness of the text.                                                                                |
| [text.antiAliasThickness](#_bookmark971) | A float value that specifies the anti-aliasing thickness of the text.                                                                                |
| [text.autoExpand](#_bookmark972)         | A Boolean value that controls the expansion of the bounding width for static text fields or the bounding width and height for dynamic or input text. |
| [text.border](#_bookmark973)             | A Boolean value that controls whether Flash shows (true) or hides (false) a border around dynamic or input text.                                     |
| [text.description](#_bookmark974)        | A string that is equivalent to the Description field in the Accessibility panel.                                                                     |

<table><thead><tr class="header"><th><strong>Property</strong></th><th><strong>Description</strong></th></tr></thead><tbody><tr class="odd"><td><a href="#_bookmark975">text.embeddedCharacters</a></td><td>A string that specifies characters to embed. This is equivalent to entering text in the Character Embedding dialog box.</td></tr><tr class="even"><td><a href="#_bookmark976">text.embedRanges</a></td><td>A string that consists of delimited integers that correspond to the items that can be selected in the Character Embedding dialog box.</td></tr><tr class="odd"><td><a href="#_bookmark977">text.embedVariantGlyphs</a></td><td>A Boolean value that specifies whether to enable the embedding of variant glyphs.</td></tr><tr class="even"><td><a href="#_bookmark979">text.filters</a></td><td>An array of filters applied to the text element</td></tr><tr class="odd"><td><a href="#_bookmark980">text.fontRenderingMode</a></td><td>A string that specifies the rendering mode for the text.</td></tr><tr class="even"><td><a href="#_bookmark983">text.length</a></td><td>Read-only; an integer that represents the number of characters in the Text object.</td></tr><tr class="odd"><td><a href="#_bookmark984">text.lineType</a></td><td><p>A string that sets the line type to "single line", "multiline", "multiline no wrap", or</p><p>"password".</p></td></tr><tr class="even"><td><a href="#_bookmark985">text.maxCharacters</a></td><td>An integer that specifies the maximum characters the user can enter into this Text object.</td></tr><tr class="odd"><td><a href="#_bookmark986">text.orientation</a></td><td>A string that specifies the orientation of the text field.</td></tr><tr class="even"><td><a href="#_bookmark987">text.renderAsHTML</a></td><td>A Boolean value that controls whether Flash draws the text as HTML and interprets embedded HTML tags.</td></tr><tr class="odd"><td><a href="#_bookmark988">text.scrollable</a></td><td>A Boolean value that controls whether the text can (true) or cannot (false) be scrolled.</td></tr><tr class="even"><td><a href="#_bookmark989">text.selectable</a></td><td>A Boolean value that controls whether the text can (true) or cannot (false) be selected. Input text is always selectable.</td></tr><tr class="odd"><td><a href="#_bookmark990">text.selectionEnd</a></td><td>A zero-based integer that specifies the offset of the end of a text subselection.</td></tr><tr class="even"><td><a href="#_bookmark991">text.selectionStart</a></td><td>A zero-based integer that specifies the offset of the beginning of a text subselection.</td></tr><tr class="odd"><td><a href="#_bookmark994">text.shortcut</a></td><td>A string that is equivalent to the Shortcut field in the Accessibility panel.</td></tr><tr class="even"><td><a href="#_bookmark995">text.silent</a></td><td>A Boolean value that specifies whether the object is accessible.</td></tr><tr class="odd"><td><a href="#_bookmark996">text.tabIndex</a></td><td>An integer that is equivalent to the Tab Index field in the Accessibility panel.</td></tr><tr class="even"><td><a href="#_bookmark997">text.textRuns</a></td><td>Read-only; an array of TextRun objects.</td></tr><tr class="odd"><td><a href="#_bookmark999">text.textType</a></td><td><p>A string that specifies the type of text field. Acceptable values are "static", "dynamic", and</p><p>"input".</p></td></tr><tr class="even"><td><a href="#_bookmark1000">text.useDeviceFonts</a></td><td>A Boolean value. A value of true causes Flash to draw text using device fonts.</td></tr><tr class="odd"><td><a href="#_bookmark1001">text.variableName</a></td><td>A string that contains the contents of the Text object.</td></tr></tbody></table>

<span id="text.accName" class="anchor"></span>
