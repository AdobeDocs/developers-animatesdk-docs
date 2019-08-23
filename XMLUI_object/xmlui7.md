## xmlui.setControlItemElement()

#### Availability

Flash 8.

#### Usage

xmlui.setControlItemElement(controlPropertyName, elementItem)

#### Parameters

**controlPropertyName** A string that specifies the control item element to set.
**elementItem** A JavaScript object with a string property named label and an optional string property named value. If the value property does not exist, then it is created and assigned the same value as label.

#### Returns

Nothing.

#### Description

Method; sets the label and value of the currently selected line in the ListBox or ComboBox control specified by
*controlPropertyName*.

#### Example

```javascript
The following example sets the label and value for the current item of the control property named PhoneNumber:
var elem = new Object(); elem.label = "Fax"; elem.value = "707-555-5555";
fl.xmlui.setControlItemElement("PhoneNumber",elem);

```
#### See also

[fl.xmlui](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl81.md)/fl81.md), [document.xmlPanel()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docu6198.md), [xmlui.getControlItemElement()](#!AdobeDocs/developers-animatesdk-docs/test/XMLUI_object/xmlui3.md), [xmlui.set()](#!AdobeDocs/developers-animatesdk-docs/test/XMLUI_object/xmlui6.md), [xmlui.setControlItemElements()](#!AdobeDocs/developers-animatesdk-docs/test/XMLUI_object/xmlui8.md))

<span id="xmlui.setControlItemElements()" class="anchor"></span>
