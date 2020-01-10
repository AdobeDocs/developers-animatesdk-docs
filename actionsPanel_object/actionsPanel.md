## actionsPanel.getClassForObject() - dropped

#### Availability

Flash CS3 Professional. *Dropped in Adobe Animate*.

#### Usage

actionsPanel.getClassForObject(ASvariableName)

#### Parameters

**ASvariableName** A string that represents the name of an ActionScript variable.

#### Returns

A string that represents the class of which *ASvariableName* is a member.

#### Description

*Dropped in Adobe Animate.*
Method; returns the class of the specified variable, which must be defined in the currently displayed Actions panel. In addition, the cursor or selected text in the Actions panel must be positioned after the variable definition.

#### Example

The following example displays the class assigned to the variable myVar, if the cursor is positioned after the statement var myVar:ActivityEvent; in the Actions panel.
```javascript
// Place the following code in the Actions panel,
// and position the cursor somewhere after the end of the line var myVar:ActivityEvent;
// Place the following code in the JSFL file
var theClass = fl.actionsPanel.getClassForObject("myVar");
fl.trace(theClass);
// traces: "ActivityEvent"
```