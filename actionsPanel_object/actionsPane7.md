## actionsPanel.setSelection()

#### Availability

Flash CS3 Professional.

#### Usage

actionsPanel.setSelection(startIndex, numberOfChars)

#### Parameters

**startIndex** A zero-based integer that specifies the first character to be selected.
**numberOfChars** An integer that specifies how many characters to select.

#### Returns

A Boolean value that specifies whether the requested characters can be selected (true) or not (false).

#### Description

Method; selects a specified set of characters in the Actions panel.

#### Example

```javascript
The following example replaces the characters "2006" in the Actions panel with the specified text.
// Type the following as the first line in the Actions panel
// 2006 - Addresses user request 40196
// Type the following in the JSFL file fl.actionsPanel.setSelection(3,4); fl.actionsPanel.replaceSelectedText("// Last updated: 2007");

```
#### See also

[actionsPanel.getSelectedText()](../actionsPanel_object/actionsPane2.md), [actionsPanel.hasSelection()](../actionsPanel_object/actionsPane4.md), [actionsPanel.replaceSelectedText()](../actionsPanel_object/actionsPane5.md)
