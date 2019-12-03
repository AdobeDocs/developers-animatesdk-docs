## textAttrs.autoKern

#### Availability

Flash MX 2004.

#### Usage

*textAttrs.autoKern*

#### Description

Property; a Boolean value that determines whether Flash uses *(true)* or ignores *(false)* pair kerning information in the font(s) when it kerns the text.

#### Example

The following example selects the characters from index 2 up to, but not including, index 6 and sets the *autoKern* property to true:

```javascript
fl.getDocumentDOM().setTextSelection(3, 6); 
fl.getDocumentDOM().setElementTextAttr('autoKern', true);

```