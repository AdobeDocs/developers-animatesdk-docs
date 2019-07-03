## text.setTextAttr()

#### Availability

Flash MX 2004.

#### Usage

text.setTextAttr(attrName, attrValue \[, startIndex \[, endIndex\]\])

#### Parameters

**attrName** A string that specifies the name of the TextAttrs object property to change.
**attrValue** The value for the TextAttrs object property.
For a list of possible values for *attrName* and *attrValue*, see the Property summary for the [TextAttrs object](#_bookmark1003).
**startIndex** An integer that is the index (zero-based) of the first character in the array. This parameter is optional.
**endIndex** An integer that specifies the index of the end point in the selected text string, which starts at *startIndex* and goes up to, but does not include, *endIndex*. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; sets the attribute specified by the *attrName* parameter associated with the text identified by *startIndex* and *endIndex* to the value specified by *attrValue*. This method can be used to change attributes of text that might span TextRun elements (see [TextRun object](#_bookmark1024)), or that are portions of existing TextRun elements. Using it may change the position and number of TextRun elements within this object’s text.textRuns array (see [text.textRuns](#_bookmark997)).
If you omit the optional parameters, the method uses the entire Text object’s character range. If you specify only *startIndex*, the range is a single character at that position. If you specify both *startIndex* and *endIndex*, the range starts from *startIndex* and goes up to, but does not include, the character located at *endIndex*.

#### Example

```
The following example sets the selected text field to italic: fl.getDocumentDOM().selection\[0\].setTextAttr("italic", true); The following example sets the size of the third character to 10: fl.getDocumentDOM().selection\[0\].setTextAttr("size", 10, 2);
The following example sets the color to red for the third through the eighth character of the selected text:
fl.getDocumentDOM().selection\[0\].setTextAttr("fillColor", 0xff0000, 2, 8);

```