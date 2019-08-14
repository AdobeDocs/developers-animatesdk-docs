## swfPanel summary

#### Availability

Flash CS4 Professional.

#### Description

The swfPanel object represents a Window SWF panel. Window SWF panels are SWF files that implement applications you can run from the Flash authoring environment; they are available from the Window \Other Panels menu. By default, Window SWF panels are stored in a subfolder of the Configuration folder (see ["Saving JSFL files" on page 2](#_bookmark3)). For example, on Windows XP, the folder is in *boot drive*\\Documents and Settings\\*user*\\Local Settings\\Application Data\\Adobe\\Flash CS4\\*language*\\Configuration\\WindowSWF. A sample Window SWF panel is available; see ["Sample Trace Bitmap panel" on page 17](#_bookmark11). The array of registered Window SWF panels is stored in the [fl.swfPanels](#!AdobeDocs/developers-animatesdk-docs/master/flash_object_(fl)/fl74.md) property.

#### Method summary

You can use the following method with the swfPanel object:

| **Method**                           | **Description**                                                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [swfPanel.call()](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPanel.md))  | Works in conjunction with the ActionScript ExternalInterface.addCallback() and MMExecute() methods to communicate with the SWF panel from the authoring environment. |
| [swfPanel.reload()](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane5.md)   | Reloads content in the SWF panel.                                                                                                                                    |
| [swfPanel.setFocus()](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane6.md) | Sets the keyboard focus to the specified SWF panel.                                                                                                                  |

#### Property summary

You can use the following properties with the swfPanel object:

| **Property**                              | **Description**                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| [swfPanel.dpiScaleFactorX](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane1.md) | A string that contains the DPI scale factor (scaleX) for swfPanel.                                   |
| [swfPanel.dpiScaleFactorY](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane2.md) | A string that contains the DPI scale factor (scaleY) for swfPanel.                                   |
| [swfPanel.name](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane3.md)            | Read-only; a string that represents the name of the specified Window SWF panel.                      |
| [swfPanel.path](#!AdobeDocs/developers-animatesdk-docs/master/swfPanel_object/swfPane4.md)            | Read-only; a string that represents the path to the SWF file used in the specified Window SWF panel. |

<span id="swfPanel.call()" class="anchor"></span>

