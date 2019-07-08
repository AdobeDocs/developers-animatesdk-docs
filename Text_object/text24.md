## text.shortcut

#### Availability

Flash MX 2004.

#### Usage

text.shortcut

#### Description

Property; a string that is equivalent to the Shortcut field in the Accessibility panel. The shortcut is read by the screen reader. This property cannot be used with dynamic text.

#### Example

```javascript
The following example gets the shortcut key of the selected object and shows the value:
var theShortcut = fl.getDocumentDOM().selection\[0\].shortcut; fl.trace(theShortcut);
The following example sets the shortcut key of the selected object:
fl.getDocumentDOM().selection\[0\].shortcut = "Ctrl+i";

```