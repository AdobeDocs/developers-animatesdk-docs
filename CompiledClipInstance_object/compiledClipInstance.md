## compiledClipInstance.accName

#### Availability

Flash MX 2004.

#### Usage

compiledClipInstance.accName

#### Description

Property; a string that is equivalent to the Name field in the Accessibility panel. Screen readers identify objects by reading the name aloud.

#### Example

The following example gets and sets the accessibility name of the first selected object:
```javascript
// Get the name of the object.
var theName = fl.getDocumentDOM().selection[0].accName;
// Set the name of the object.
fl.getDocumentDOM().selection[0].accName = 'Home Button';
```