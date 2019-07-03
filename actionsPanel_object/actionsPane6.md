## actionsPanel.setScriptAssistMode() - dropped

#### Availability

Flash CS3 Professional. *Dropped in Adobe Animate*.

#### Usage

actionsPanel.setScriptAssistMode(bScriptAssist)

#### Parameters

**bScriptAssist** A Boolean value that specifies whether to enable or disable Script Assist mode.

#### Returns

A Boolean value that specifies whether Script Assist mode was enabled or disabled successfully.

#### Description

*Dropped in Adobe Animate.*
Method; enables or disables Script Assist mode.

#### Example

```
The following example toggles the state of Script Assist mode.
fl.trace(fl.actionsPanel.getScriptAssistMode()); if (fl.actionsPanel.getScriptAssistMode()){
fl.actionsPanel.setScriptAssistMode(false);
}
else {
fl.actionsPanel.setScriptAssistMode(true);
}
fl.trace(fl.actionsPanel.getScriptAssistMode());

```
#### See also

[actionsPanel.getScriptAssistMode() - dropped](#_bookmark34)
