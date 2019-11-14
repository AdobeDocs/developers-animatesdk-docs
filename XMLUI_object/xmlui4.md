## xmlui.getEnabled()

#### Availability

Flash 8.

#### Usage

xmlui.getEnabled(controlID)

#### Parameters

**controlID** A string that specifies the ID attribute of the control whose status you want to retrieve.

#### Returns

A Boolean value of true if the control is enabled; false otherwise.

#### Description

Method; returns a Boolean value that specifies whether the control is enabled or disabled (dimmed).

#### Example

```javascript
The following example returns a value that indicates whether the control with the ID attribute myListBox is enabled:
var isEnabled = fl.xmlui.getEnabled("myListBox"); fl.trace(isEnabled);

```
#### See also

[fl.xmlui](../flash_object_(fl)/fl81.md)/fl81.md), [document.xmlPanel()](../Document_object/docu6198.md), [xmlui.setEnabled()](../XMLUI_object/xmlui9.md)
