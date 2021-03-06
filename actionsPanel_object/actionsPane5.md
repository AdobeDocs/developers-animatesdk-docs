## actionsPanel.replaceSelectedText()

#### Availability

Flash CS3 Professional.

#### Usage

actionsPanel.replaceSelectedText(replacementText)

#### Parameters

**replacementText** A string that represents text to replace selected text in the Actions panel.

#### Returns

A Boolean value of true if the Actions panel is found; false otherwise.

#### Description

Method; replaces the currently selected text with the text specified in *replacementText*. If *replacementText* contains more characters than the selected text, any characters following the selected text now follow *replacementText*; that is, they are not overwritten.

#### Example

The following example replaces currently selected text in the Actions panel.
```javascript
if (fl.actionsPanel.hasSelection()) {
fl.actionsPanel.replaceSelectedText("// © 2006 Adobe Inc.");
}
```
#### See also

[actionsPanel.getSelectedText()](../actionsPanel_object/actionsPane2.md), [actionsPanel.hasSelection()](../actionsPanel_object/actionsPane4.md), [actionsPanel.setSelection()](../actionsPanel_object/actionsPane7.md), [actionsPanel.setText()](../actionsPanel_object/actionsPane8.md)
