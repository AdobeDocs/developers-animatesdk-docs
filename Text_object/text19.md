## text.selectable

#### Availability

Flash MX 2004.

#### Usage

text.selectable

#### Description

Property; a Boolean value. If the value is true, the text can be selected.

Input text is always selectable. Flash generates a warning when this property is set to false and used with input text.

#### Example

The following example sets the selectable property to true:
```javascript
 fl.getDocumentDOM().selection[0].selectable = true;
```