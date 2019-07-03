## textAttrs.letterSpacing

#### Availability

Flash 8.

#### Usage

textAttrs.letterSpacing

#### Description

Property; an integer that represents the space between characters. Acceptable values are -60 through 60. This property applies only to static text; it generates a warning if used with other text types.

#### Example

```
The following code selects the characters from index 0 up to but not including index 10 and sets the character spacing to 60:
fl.getDocumentDOM().setTextSelection(0, 10);
fl.getDocumentDOM().setElementTextAttr("letterSpacing", 60);

```