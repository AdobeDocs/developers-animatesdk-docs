## xmlui summary

#### Availability

Flash MX 2004.

#### Description

Flash 8 supports custom dialog boxes written in a subset of the XML User Interface Language (XUL). An XML User Interface (XMLUI) dialog box can be used by several Flash features, such as commands and behaviors, to provide a user interface for features that you build using extensibility. The XMLUI object provides the ability to get and set properties of an XMLUI dialog box, and accept or cancel out of one. The XMLUI methods can be used in callbacks, such as oncommand handlers in buttons.
>
You can write a dialog.xml file and invoke it from the JavaScript API using the [document.xmlPanel()](#_bookmark342) method. To retrieve an object representing the current XMLUI dialog box, use [fl.xmlui](#_bookmark557).

#### Method summary

The following methods are available for the XMLUI object:

| **Method**                                       | **Description**                                                                             |
|--------------------------------------------------|---------------------------------------------------------------------------------------------|
| [xmlui.accept()](#xmlui.accept())                | Closes the current XMLUI dialog box with an accept state.                                   |
| [xmlui.cancel()](#_bookmark1154)                 | Closes the current XMLUI dialog box with a cancel state.                                    |
| [xmlui.get()](#_bookmark1155)                    | Retrieves the value of the specified property of the current XMLUI dialog box.              |
| [xmlui.getControlItemElement()](#_bookmark1156)  | Returns the current control item for the specified control.                                 |
| [xmlui.getEnabled()](#_bookmark1157)             | Returns a Boolean value that specifies whether the control is enabled or disabled (dimmed). |
| [xmlui.getVisible()](#_bookmark1158)             | Returns a Boolean value that specifies whether the control is visible or hidden.            |
| [xmlui.set()](#_bookmark1159)                    | Modifies the value of the specified property of the current XMLUI dialog box.               |
| [xmlui.setControlItemElement()](#_bookmark1160)  | Sets the label and value for the current item.                                              |
| [xmlui.setControlItemElements()](#_bookmark1161) | Sets the label, value pairs of the current item.                                            |
| [xmlui.setEnabled()](#_bookmark1162)             | Enables or disables (dims) a control.                                                       |
| [xmlui.setVisible()](#_bookmark1163)             | Shows or hides a control.                                                                   |

<span id="xmlui.accept()" class="anchor"></span>

