## document.accName

#### Availability

Flash MX 2004.

#### Usage

document.accName

#### Description

Property; a string that is equivalent to the Name field in the Accessibility panel. Screen readers identify objects by reading the name aloud.

#### Example

```javascript
The following example sets the accessibility name of the document to "Main Movie": fl.getDocumentDOM().accName = "Main Movie";
The following example gets the accessibility name of the document:
fl.trace(fl.getDocumentDOM().accName);

```