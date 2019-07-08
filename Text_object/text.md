## text.accName

#### Availability

Flash MX 2004.

#### Usage

text.accName

#### Description

Property; a string that is equivalent to the Name field in the Accessibility panel. Screen readers identify objects by reading the name aloud. This property cannot be used with dynamic text.

#### Example

```javascript
The following example retrieves the name of the object:
var doc = fl.getDocumentDOM();
var theName = doc.selection\[0\].accName;
The following example sets the name of the currently selected object:
fl.getDocumentDOM().selection\[0\].accName = "Home Button";

```