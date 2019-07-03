## xmlui.get()

#### Availability

Flash MX 2004.

#### Usage

xmlui.get(controlPropertyName)

#### Parameters

**controlPropertyName** A string that specifies the name of the XMLUI property whose value you want to retrieve.

#### Returns

A string that represents the value of the specified property. In cases where you might expect a Boolean value of true
>
or false, it returns the string "true" or "false".

#### Description

Method; retrieves the value of the specified property of the current XMLUI dialog box.

#### Example

```
The following example returns the value of a property named URL: fl.xmlui.get("URL");

```
#### See also

[fl.xmlui](#_bookmark557), [document.xmlPanel()](#_bookmark342), [xmlui.getControlItemElement()](#xmlui.getControlItemElement()), [xmlui.set()](#_bookmark1159)

<span id="xmlui.getControlItemElement()" class="anchor"></span>
