## textAttrs.indent

#### Availability

Flash MX 2004.

#### Usage

textAttrs.indent

#### Description

Property; an integer that specifies paragraph indentation. Acceptable values are -720 through 720.

#### Example

```javascript
The following example sets the indentation of the selected text field from the character at index 2 up to, but not including, the character at index 8 to 100. This can affect characters outside the specified range if they are in the same paragraph.
fl.getDocumentDOM().selection\[0\].setTextAttr("indent", 100, 2, 8);

```