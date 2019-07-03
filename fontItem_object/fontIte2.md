## fontItem.embeddedCharacters

#### Availability

Flash CS5 Professional.

#### Usage

fontItem.embeddedCharacters

#### Description

Property; a string value that allows you to specify characters to embed within a SWF file so that the characters do not need to be present on the devices the SWF file eventually plays back on. This property provides the same functionality as the Font Embedding dialog box.
>
This property can also be read, allowing you to find out what characters were specified with the Font Embedding dialog box for a given Font item.

#### Example

```
Assuming that the first item in the Library is a Font item, the following code embeds the characters a, b, and c.
fl.getDocumentDOM().library.items\[0\].embeddedCharacters = "abc";

```