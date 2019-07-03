## document.setElementTextAttr()

#### Availability

Flash MX 2004.

#### Usage

document.setElementTextAttr(attrName, attrValue \[, startIndex \[, endIndex\]\])

#### Parameters

**attrName** A string that specifies the name of the TextAttrs property to change.
**attrValue** The value to which to set the TextAttrs property. For a list of property names and expected values, see the Property summary table for the [TextAttrs object](#_bookmark1003).
**startIndex** An integer value that specifies the index of the first character that is affected. This parameter is optional.
**endIndex** An integer value that specifies the index of the last character that is affected. This parameter is optional.

#### Returns

A Boolean value: true if at least one text attribute property is changed; false otherwise.

#### Description

Method; sets the specified textAttrs property of the selected text items to the specified value. For a list of property names and allowable values, see the Property summary table for the [TextAttrs object](#_bookmark1003). If the optional parameters are not passed, the method sets the style of the currently selected text range, or the whole text field if no text is selected. If only *startIndex* is passed, the method sets that character’s attributes. If *startIndex* and *endIndex* are passed, the method sets the attributes on the characters starting from *startIndex* up to, but not including, *endIndex*. If paragraph styles are specified, all the paragraphs that fall within the range are affected.

#### Example

```
The following examples set the fillColor, italic, and bold text attributes for the selected text items:
var success = fl.getDocumentDOM().setElementTextAttr("fillColor", "\#00ff00"); var pass = fl.getDocumentDOM().setElementTextAttr("italic", true, 10);
var ok = fl.getDocumentDOM().setElementTextAttr("bold", true, 5, 15);

```