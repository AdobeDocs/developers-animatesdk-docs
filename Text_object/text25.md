## text.silent

#### Availability

Flash MX 2004.

#### Usage

text.silent

#### Description

Property; a Boolean value that specifies whether the object is accessible. This is equivalent to the inverse logic of the Make Object Accessible setting in the Accessibility panel. That is, if silent is true, Make Object Accessible is deselected. If it is false, Make Object Accessible is selected.

#### Example

The following example determines if the object is accessible (a value of false means that it is accessible):
```javascript
var isSilent = fl.getDocumentDOM().selection[0].silent; 
```
The following example sets the object to be accessible: 
```javascript
fl.getDocumentDOM().selection[0].silent = false;
```