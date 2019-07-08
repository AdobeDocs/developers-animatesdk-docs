## actionsPanel.getScriptAssistMode() - dropped

#### Availability

Flash CS3 Professional. *Dropped in Adobe Animate*.

#### Usage

actionsPanel.getScriptAssistMode()

#### Parameters

None.

#### Returns

A Boolean value that specifies whether Script Assist mode is enabled (true) or not (false).

#### Description

*Dropped in Adobe Animate.*
Method; specifies whether Script Assist mode is enabled.

#### Example

```javascript
The following example displays a message if Script Assist mode is not enabled.
mAssist = fl.actionsPanel.getScriptAssistMode(); if (!mAssist) {
alert("For more guidance when writing ActionScript code, try Script Assist mode");
}

```
#### See also

[actionsPanel.setScriptAssistMode() - dropped](#_bookmark39)
