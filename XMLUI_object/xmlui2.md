## xmlui.get()

#### Availability

Flash MX 2004.

#### Usage

xmlui.get(controlPropertyName)

#### Parameters

**controlPropertyName** A string that specifies the name of the XMLUI property whose value you want to retrieve.

#### Returns

A string that represents the value of the specified property. In cases where you might expect a Boolean value of true
or false, it returns the string "true" or "false".

#### Description

Method; retrieves the value of the specified property of the current XMLUI dialog box.

#### Example

```javascript
The following example returns the value of a property named URL: fl.xmlui.get("URL");

```
#### See also

[fl.xmlui](#!AdobeDocs/developers-animatesdk-docs/master/flash_object_(fl)/fl81.md), [document.xmlPanel()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docu6198.md), [xmlui.getControlItemElement()](#!AdobeDocs/developers-animatesdk-docs/master/XMLUI_object/xmlui3.md)), [xmlui.set()](#!AdobeDocs/developers-animatesdk-docs/master/XMLUI_object/xmlui6.md)

<span id="xmlui.getControlItemElement()" class="anchor"></span>
