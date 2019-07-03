## textAttrs.aliasText

#### Availability

Flash MX 2004.

#### Usage

textAttrs.aliasText

#### Description

Property; a Boolean value that specifies that Flash should draw the text using a method optimized for increasing the legibility of small text.

#### Example

```
The following example sets the aliasText property to true for all the text in the currently selected text field:
fl.getDocumentDOM().setElementTextAttr('aliasText', true);

```