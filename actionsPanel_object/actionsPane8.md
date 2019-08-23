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

```javascript
The following example replaces any text currently in the Actions panel with the specified text.
fl.actionsPanel.setText("// Deleted this code - no longer needed");

```
#### See also

[actionsPanel.getText()](#!AdobeDocs/developers-animatesdk-docs/master/actionsPanel_object/actionsPane3.md), [actionsPanel.replaceSelectedText()](#!AdobeDocs/developers-animatesdk-docs/master/actionsPanel_object/actionsPane5.md)
