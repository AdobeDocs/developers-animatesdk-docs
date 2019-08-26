## text.selectionStart

#### Availability

Flash MX 2004.

#### Usage

text.selectionStart

#### Description

Property; a zero-based integer that specifies the beginning of a text subselection. You can use this property with text.selectionEnd to select a range of characters. Characters up to, but not including, text.selectionEnd are selected. See [text.selectionEnd](#!AdobeDocs/developers-animatesdk-docs/test/Text_object/text20.md).

-   If there is an insertion point or no selection, text.selectionEnd is equal to text.selectionStart.

-   If text.selectionStart is set to a value greater than text.selectionEnd, text.selectionEnd is set to

text.selectionStart, and no text is selected.

#### Example

```javascript
The following example sets the start of the text subselection to the sixth character:
fl.getDocumentDOM().selection\[0\].selectionStart = 5;
The following example selects the characters Barbara from a text field that contains the text My name is Barbara
and formats them as bold and green:
fl.getDocumentDOM().selection\[0\].selectionStart = 11;
fl.getDocumentDOM().selection\[0\].selectionEnd = 18;
var s = fl.getDocumentDOM().selection\[0\].selectionStart; var e = fl.getDocumentDOM().selection\[0\].selectionEnd; fl.getDocumentDOM().setElementTextAttr('bold', true, s, e);
fl.getDocumentDOM().setElementTextAttr("fillColor", "\#00ff00", s, e);

```