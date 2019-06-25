## textAttrs.characterPosition

#### Availability

> Flash MX 2004.

#### Usage

> textAttrs.characterPosition

#### Description

> Property; a string that determines the baseline for the text. Acceptable values are "normal", "subscript", and
>
> "superscript". This property applies only to static text.

#### Example

> The following example selects the characters from index 2 up to, but not including, index 6 of the selected text field and sets the characterPosition property to subscript:
>
> fl.getDocumentDOM().setTextSelection(2, 6); fl.getDocumentDOM().setElementTextAttr("characterPosition", "subscript");
