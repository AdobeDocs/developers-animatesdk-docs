## xmlui.setControlItemElements()

#### Availability

Flash 8.

#### Usage

xmlui.setControlItemElements(controlID, elementItemArray)

#### Parameters

**controlID** A string that specifies the ID attribute of the control you want to set.
**elementItemArray** An array of JavaScript objects, where each object has a string property named label and an optional string property named value. If the value property does not exist, then it is created and assigned the same value as label.

#### Returns

Nothing.

#### Description

Method; clears the values of the ListBox or ComboBox control specified by *controlID* and replaces the list or menu items with the label, value pairs specified by *elementItemArray*.

#### Example

```
The following example sets the label and value of items in the control with the ID attribute myControlID to the label, value pairs specified:
var nameArray = new Array("January", "February", "March"); var monthArray = new Array();
for (i=0;i\<nameArray.length;i++){ elem = new Object(); elem.label = nameArray\[i\]; elem.value = i;
monthArray\[i\] = elem;
}
fl.xmlui.setControlItemElements("myControlID", monthArray);

```
#### See also

[xmlui.getControlItemElement()](#_bookmark1156), [xmlui.set()](#_bookmark1159), [xmlui.setControlItemElement()](#_bookmark1160)
