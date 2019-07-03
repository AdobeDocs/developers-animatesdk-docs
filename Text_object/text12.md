## text.getTextString()

#### Availability

Flash MX 2004.

#### Usage

text.getTextString(\[startIndex \[, endIndex\]\])

#### Parameters

**startIndex** An integer that specifies the index (zero-based) of the first character. This parameter is optional.
**endIndex** An integer that specifies the end of the range of text, which starts from *startIndex* and goes up to, but does not include, *endIndex*. This parameter is optional.

#### Returns

A string of the text in the specified range.

#### Description

Method; retrieves the specified range of text. If you omit the optional parameters *startIndex* and *endIndex*, the whole text string is returned. If you specify only *startIndex*, the method returns the string starting at the index location and ending at the end of the field. If you specify both *startIndex* and *endIndex*, the method returns the string starting from *startIndex* and goes up to, but does not include, *endIndex*.

#### Example

```
The following example gets the character(s) from the fifth character through the end of the selected text field:
var myText = fl.getDocumentDOM().selection\[0\].getTextString(4); fl.trace(myText);
The following example gets the fourth through the ninth characters starting in the selected text field:
var myText = fl.getDocumentDOM().selection\[0\].getTextString(3, 9); fl.trace(myText);

```