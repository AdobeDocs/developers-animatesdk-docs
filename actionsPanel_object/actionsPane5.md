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

```
The following example replaces currently selected text in the Actions panel.
if (fl.actionsPanel.hasSelection()) { fl.actionsPanel.replaceSelectedText("// © 2006 Adobe Inc.");
}

```
#### See also

[actionsPanel.getSelectedText()](#_bookmark35), [actionsPanel.hasSelection()](#_bookmark37), [actionsPanel.setSelection()](#_bookmark40), [actionsPanel.setText()](#_bookmark41)
