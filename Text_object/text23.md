## text.setTextString()

#### Availability

Flash MX 2004.

#### Usage

text.setTextString(text \[, startIndex \[, endIndex\]\])

#### Parameters

**text** A string that consists of the characters to be inserted into this Text object.
**startIndex** An integer that specifies the index (zero-based) of the character in the string where the text will be inserted. This parameter is optional.
**endIndex** An integer that specifies the index of the end point in the selected text string. The new text overwrites the text from *startIndex* up to, but not including, *endIndex*. This parameter is optional.

#### Returns

Nothing.

#### Description

Property; changes the text string within this Text object. If you omit the optional parameters, the whole Text object is replaced. If you specify only *startIndex*, the specified string is inserted at the *startIndex* position. If you specify both *startIndex* and *endIndex*, the specified string replaces the segment of text starting from *startIndex* up to, but not including, *endIndex*.

#### Example

```
The following example assigns the string this is a string to the selected text field:
fl.getDocumentDOM().selection\[0\].setTextString("this is a string");
The following example inserts the string abc beginning at the fifth character of the selected text field:
fl.getDocumentDOM().selection\[0\].setTextString("01234567890"); fl.getDocumentDOM().selection\[0\].setTextString("abc", 4);
// text field is now "0123abc4567890"
The following example replaces the text from the third through the eighth character of the selected text string with the string abcdefghij. Characters between *startIndex* and *endIndex* are overwritten. Characters beginning with *endIndex* follow the inserted string.
fl.getDocumentDOM().selection\[0\].setTextString("01234567890"); fl.getDocumentDOM().selection\[0\].setTextString("abcdefghij", 2, 8);
// text field is now "01abcdefghij890"

```