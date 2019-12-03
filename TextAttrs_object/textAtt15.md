## textAttrs.size

#### Availability

Flash MX 2004.

#### Usage

*textAttrs.size*

#### Description

Property; an integer that specifies the size of the font.

#### Example

The following example retrieves the size of the character at index 2 and shows the result in the Output panel:

```javascript
fl.outputPanel.trace(fl.getDocumentDOM().selection[0].getTextAttr("size", 2));

```