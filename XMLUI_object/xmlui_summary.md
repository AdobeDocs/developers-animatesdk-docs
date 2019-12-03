## xmlui summary

#### Availability

Flash MX 2004.

#### Description

Flash 8 supports custom dialog boxes written in a subset of the XML User Interface Language (XUL). An XML User Interface (XMLUI) dialog box can be used by several Flash features, such as commands and behaviors, to provide a user interface for features that you build using extensibility. The XMLUI object provides the ability to get and set properties of an XMLUI dialog box, and accept or cancel out of one. The XMLUI methods can be used in callbacks, such as *oncommand* handlers in buttons.
You can write a dialog.xml file and invoke it from the JavaScript API using the [document.xmlPanel()](../Document_object/docu6198.md) method. To retrieve an object representing the current XMLUI dialog box, use [fl.xmlui](../flash_object_(fl)/fl81.md).

#### Method summary

The following methods are available for the XMLUI object:

| **Method**                                       | **Description**                                                                             |
|--------------------------------------------------|---------------------------------------------------------------------------------------------|
| [xmlui.accept()](../XMLUI_object/xmlui.md)                | Closes the current XMLUI dialog box with an accept state.                                   |
| [xmlui.cancel()](../XMLUI_object/xmlui1.md)                 | Closes the current XMLUI dialog box with a cancel state.                                    |
| [xmlui.get()](../XMLUI_object/xmlui2.md)                    | Retrieves the value of the specified property of the current XMLUI dialog box.              |
| [xmlui.getControlItemElement()](../XMLUI_object/xmlui3.md)  | Returns the current control item for the specified control.                                 |
| [xmlui.getEnabled()](../XMLUI_object/xmlui4.md)             | Returns a Boolean value that specifies whether the control is enabled or disabled (dimmed). |
| [xmlui.getVisible()](../XMLUI_object/xmlui5.md)             | Returns a Boolean value that specifies whether the control is visible or hidden.            |
| [xmlui.set()](../XMLUI_object/xmlui6.md)                    | Modifies the value of the specified property of the current XMLUI dialog box.               |
| [xmlui.setControlItemElement()](../XMLUI_object/xmlui7.md)  | Sets the label and value for the current item.                                              |
| [xmlui.setControlItemElements()](../XMLUI_object/xmlui8.md) | Sets the label, value pairs of the current item.                                            |
| [xmlui.setEnabled()](../XMLUI_object/xmlui9.md)             | Enables or disables (dims) a control.                                                       |
| [xmlui.setVisible()](../XMLUI_object/xmlui10.md)             | Shows or hides a control.                                                                   |

<span id="xmlui.accept()" class="anchor"></span>

