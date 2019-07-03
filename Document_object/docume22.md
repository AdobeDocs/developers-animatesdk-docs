## document.autoLabel

#### Availability

Flash MX 2004.

#### Usage

document.autoLabel

#### Description

Property; a Boolean value that is equivalent to the Auto Label check box in the Accessibility panel. You can use this property to tell Flash to automatically label objects on the Stage with the text associated with them.

#### Example

```
The following example gets the value of the autoLabel property and displays the result in the Output panel:
var isAutoLabel = fl.getDocumentDOM().autoLabel; fl.trace(isAutoLabel);
The following example sets the autoLabel property to true, telling Flash to automatically label objects on the Stage:
fl.getDocumentDOM().autoLabel = true;

```