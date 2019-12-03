## textAttrs.characterSpacing

#### Availability

Flash MX 2004. Deprecated in Flash 8 in favor of [textAttrs.letterSpacing](../TextAttrs_object/textAtt11.md).

#### Usage

*textAttrs.characterSpacing*

#### Description

Property; an integer that represents the space between characters. Acceptable values are -60 through 60. 

This property applies only to static text; it generates a warning if used with other text types.

#### Example

The following example sets the character spacing of the selected text field to 10:

```javascript
fl.getDocumentDOM().setElementTextAttr("characterSpacing", 10);

```