## fontItem.italic

#### Availability

Flash CS4 Professional.

#### Usage

fontItem.italic

#### Description

Property; a Boolean value that specifies whether the Font item is italic (true) or not (false).

#### Example

 Assuming that the first item in the Library is a Font item, the following code displays true in the Output panel if it is
italic, false if it is not, and then sets it to italic.

```javascript
var theItem = fl.getDocumentDOM().library.items[0];
fl.outputPanel.clear();
fl.trace("italic: "+ theItem.italic);
theItem.italic=true;
fl.trace("italic: "+ theItem.italic);
```