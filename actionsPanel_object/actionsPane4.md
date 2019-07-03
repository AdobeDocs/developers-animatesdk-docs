## actionsPanel.hasSelection()

#### Availability

Flash CS3 Professional.

#### Usage

actionsPanel.hasSelection()

#### Parameters

None.

#### Returns

A Boolean value that specifies whether any text is selected in the Actions panel (true) or not (false).

#### Description

Method; specifies whether any text is currently selected in the Actions panel.

#### Example

```
The following example displays text that is currently selected in the Actions panel. If no text is selected, it displays all the text in the Actions panel.
if (fl.actionsPanel.hasSelection()) {
var apText = fl.actionsPanel.getSelectedText();
}
else {
var apText = fl.actionsPanel.getText();
}
fl.trace(apText);

```
#### See also

[actionsPanel.getSelectedText()](#_bookmark35), [actionsPanel.getText()](#_bookmark36), [actionsPanel.replaceSelectedText()](#actionsPanel.replaceSelectedText()), [actionsPanel.setSelection()](#_bookmark40)

<span id="actionsPanel.replaceSelectedText()" class="anchor"></span>
