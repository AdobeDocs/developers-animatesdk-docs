## document.description

#### Availability

Flash MX 2004.

#### Usage

document.description

#### Description

Property; a string that is equivalent to the Description field in the Accessibility panel. The description is read by the screen reader.

#### Example

```javascript
The following example sets the description of the document:
fl.getDocumentDOM().description= "This is the main movie";
The following example gets the description of the document and displays it in the Output panel:
fl.trace(fl.getDocumentDOM().description);

```