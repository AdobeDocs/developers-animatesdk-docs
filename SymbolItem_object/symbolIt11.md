## symbolItem.symbolType

#### Availability

Flash MX 2004.

#### Usage

*symbolItem.symbolType*

#### Description

Property; a string that specifies the type of symbol. Acceptable values are *"movie clip", "button",* and *"graphic"*.

#### Example

The following example shows the current value of the symbolType property, changes it to button, and shows it again:

```javascript
alert(fl.getDocumentDOM().library.items[0].symbolType); 
fl.getDocumentDOM().library.items[0].symbolType = "button"; 
alert(fl.getDocumentDOM().library.items[0].symbolType);

```