## text.description

#### Availability

Flash MX 2004.

#### Usage

text.description

#### Description

Property; a string that is equivalent to the Description field in the Accessibility panel. The description is read by the screen reader.

#### Example

```javascript
The following example retrieves the description of the object:
var doc = fl.getDocumentDOM();
var desc = doc.selection\[0\].description;
The following example sets the description of the object:
var doc = fl.getDocumentDOM(); doc.selection\[0\].description= "Enter your name here";

```