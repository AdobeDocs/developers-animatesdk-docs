## actionsPanel.setText()

#### Availability

Flash CS3 Professional.

#### Usage

actionsPanel.setText(replacementText)

#### Parameters

**replacementText** A string that represents text to place in the Actions panel.

#### Returns

A Boolean value of true if the specified text was placed in the Actions panel; false otherwise.

#### Description

Method; clears any text in the Actions panel and then adds the text specified in *replacementText*.

#### Example

The following example replaces any text currently in the Actions panel with the specified text.
```javascript
fl.actionsPanel.setText("// Deleted this code - no longer needed");
```
#### See also

[actionsPanel.getText()](../actionsPanel_object/actionsPane3.md), [actionsPanel.replaceSelectedText()](../actionsPanel_object/actionsPane5.md)
