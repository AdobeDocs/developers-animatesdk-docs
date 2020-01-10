## text.variableName

#### Availability

Flash MX 2004.

#### Usage

text.variableName

#### Description

Property; a string that contains the name of the variable associated with the Text object. This property works only with dynamic or input text; it generates a warning if used with other text types.

This property is supported only in ActionScript 1.0 and ActionScript 2.0.

#### Example

The following example sets the variable name of the selected text box to firstName:
```javascript
fl.getDocumentDOM().selection[0].variableName = "firstName";
```