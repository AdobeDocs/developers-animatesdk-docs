## textAttrs.lineSpacing

#### Availability

Flash MX 2004.

#### Usage

textAttrs.lineSpacing

#### Description

Property; an integer that specifies the line spacing (*leading*) of the paragraph. Acceptable values are -360 through 720.

#### Example

```javascript
The following example sets the selected text field’s lineSpacing property to 100:
fl.getDocumentDOM().selection\[0\].setTextAttr("lineSpacing", 100);

```