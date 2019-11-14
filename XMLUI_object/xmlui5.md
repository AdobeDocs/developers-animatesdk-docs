## xmlui.getVisible()

#### Availability

Flash 8.

#### Usage

xmlui.getVisible(controlID)

#### Parameters

**controlID** A string that specifies the ID attribute of the control whose visibility status you want to retrieve.

#### Returns

A Boolean value of true if the control is visible, or false if it is invisible (hidden).

#### Description

Method; returns a Boolean value that specifies whether the control is visible or hidden.

#### Example

```javascript
The following example returns a value that indicates whether the control with the ID attribute myListBox is visible:
var isVisible = fl.xmlui.getVisible("myListBox"); fl.trace(isVisible);

```
#### See also

[xmlui.setVisible()](../XMLUI_object/xmlui10.md)
