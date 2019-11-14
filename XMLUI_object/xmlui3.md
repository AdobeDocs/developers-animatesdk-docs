## xmlui.getControlItemElement()

#### Availability

Flash 8.

#### Usage

xmlui.getControlItemElement(controlPropertyName)

#### Parameters

**controlPropertyName** A string that specifies the property whose control item element you want to retrieve.

#### Returns

An object that represents the current control item for the control specified by *controlPropertyName*.

#### Description

Method; returns the label and value of the line selected in a ListBox or ComboBox control for the control specified by
*controlPropertyName*.

#### Example

```javascript
The following example returns the label and value of the currently selected line for the myListBox control:
var elem = new Object();
elem = fl.xmlui.getControlItemElement("myListBox"); fl.trace("label = " + elem.label + " value = " + elem.value);

```
#### See also

[fl.xmlui](../flash_object_(fl)/fl81.md)/fl81.md), [document.xmlPanel()](../Document_object/docu6198.md), [xmlui.get()](../XMLUI_object/xmlui2.md), [xmlui.setControlItemElement()](../XMLUI_object/xmlui7.md), [xmlui.setControlItemElements()](../XMLUI_object/xmlui8.md)
