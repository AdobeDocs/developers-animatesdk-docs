## textAttrs.leftMargin

#### Availability

Flash MX 2004.

#### Usage

textAttrs.leftMargin

#### Description

Property; an integer that specifies the paragraph’s left margin. Acceptable values are 0 through 720.

#### Example

```
The following example sets the leftMargin property of the selected text field from the character at index 2 up to, but not including, the character at index 8 to 100. This can affect characters outside the specified range if they are in the same paragraph.
fl.getDocumentDOM().selection\[0\].setTextAttr("leftMargin", 100, 2, 8);

```