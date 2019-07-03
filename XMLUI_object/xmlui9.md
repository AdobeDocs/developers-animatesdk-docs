## xmlui.setEnabled()

#### Availability

Flash 8.

#### Usage

xmlui.setEnabled(controlID, enable)

#### Parameters

**controlID** A string that specifies the ID attribute of the control you want to enable or disable.
**enable** A Boolean value of true if you want to enable the control, or false if you want to disable (dim) it.

#### Returns

Nothing.

#### Description

Method; enables or disables (dims) a control.

#### Example

```
The following example dims the control with the ID attribute myControl: fl.xmlui.setEnabled("myControl", false);

```
#### See also

[xmlui.getEnabled()](#_bookmark1157)
