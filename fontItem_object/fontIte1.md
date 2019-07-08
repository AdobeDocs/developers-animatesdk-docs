## fontItem.bold

#### Availability

Flash CS4 Professional.

#### Usage

fontItem.bold

#### Description

Property; a Boolean value that specifies whether the Font item is bold (true) or not (false).

#### Example

```javascript
Assuming that the first item in the Library is a Font item, the following code displays true in the Output panel if it is bold, false if it is not, and then sets it to bold.
var theItem = fl.getDocumentDOM().library.items\[0\]; fl.outputPanel.clear();
fl.trace("bold: "+ theItem.bold); theItem.bold=true; fl.trace("bold: "+ theItem.bold);

```