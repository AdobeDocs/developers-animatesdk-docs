## document.getTextString()

#### Availability

Flash MX 2004.

#### Usage

document.getTextString(\[startIndex \[, endIndex\]\])

#### Parameters

**startIndex** An integer that is an index of first character to get. This parameter is optional.
**endIndex** An integer that is an index of last character to get. This parameter is optional.

#### Returns

A string that contains the selected text.

#### Description

Method; gets the currently selected text. If the optional parameters are not passed, the current text selection is used. If text is not currently opened for editing, the whole text string is returned. If only *startIndex* is passed, the string starting at that index and ending at the end of the field is returned. If *startIndex* and *endIndex* are passed, the string starting from *startIndex* up to, but not including, *endIndex* is returned.
If there are several text fields selected, the concatenation of all the strings is returned.

#### Example

```javascript
The following example gets the string in the selected text fields:
fl.getDocumentDOM().getTextString();
The following example gets the string at character index 5 in the selected text fields:
fl.getDocumentDOM().getTextString(5);
The following example gets the string from character index 2 up to, but not including, character index 10:
fl.getDocumentDOM().getTextString(2, 10);

```
#### See also

[document.setTextString()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docu9908.md)
