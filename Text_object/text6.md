## text.embeddedCharacters

#### Availability

Flash MX 2004.

#### Usage

text.embeddedCharacters

#### Description

Property; a string that specifies characters to embed. This is equivalent to entering text in the Character Embedding dialog box.
This property works only with dynamic or input text; it generates a warning if used with other text types.
***Note:** Beginning in Flash Professional CS5, font embedding is controlled at the document level instead of the text object level. Use the* *["fontItem.embeddedCharacters" on page 310](#_bookmark585) property instead of the text.embeddedCharacters property.*

#### Example

```
The following example assumes that the first or only item in the current selection is a classic text object and sets the
embeddedCharacters property to abc: fl.getDocumentDOM().selection\[0\].embeddedCharacters = "abc";

```