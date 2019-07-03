## document.as3WarningsMode

#### Availability

Flash CS3 Professional.

#### Usage

document.as3WarningsMode

#### Description

Property; a Boolean value that specifies whether the ActionScript 3.0 compiler should compile with the Warnings Mode option turned on (true) or off (false). Warnings Mode causes extra warnings to be reported that are useful for discovering incompatibilities when updating ActionScript 2.0 code to ActionScript 3.0. The default value is true.

#### Example

```
The following example turns off the Warnings Mode compiler option.
var myDocument = fl.getDocumentDOM();
fl.outputPanel.trace("Warnings Mode value before modification is " + myDocument.as3WarningsMode);
myDocument.as3WarningsMode = false;
fl.outputPanel.trace("Warnings Mode value after modification is " + myDocument.as3WarningsMode);

```
#### See also

[document.as3StrictMode](#_bookmark138)
