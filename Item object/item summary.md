## item summary

#### Availability

> Flash MX 2004.

#### Description

> The Item object is an abstract base class. Anything in the library derives from Item. See also [library object](#_bookmark693).

#### Method summary

> The following methods are available for the Item object:

| **Method**                             | **Description**                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [item.addData()](#item.addData())      | Adds specified data to a library item.                                                                                         |
| [item.getData()](#_bookmark661)        | Retrieves the value of the specified data.                                                                                     |
| [item.getPublishData()](#_bookmark662) | Indicates whether publishing of the specified persistent data is enabled for the specified format on a specified library item. |
| [item.hasData()](#_bookmark663)        | Determines whether the library item has the named data.                                                                        |
| [item.removeData()](#_bookmark676)     | Removes persistent data from the library item.                                                                                 |
| [item.setPublishData()](#_bookmark677) | Enables publishing of persistent data for a library item.                                                                      |

#### Property summary

> The following properties are available for the Item object:

| **Property**                                    | **Description**                                                                                                 |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [item.itemType](#_bookmark664)                  | Read-only; a string that specifies the type of element.                                                         |
| [item.linkageBaseClass](#_bookmark666)          | A string that specifies the ActionScript 3.0 class that will be associated with the symbol.                     |
| [item.linkageClassName](#_bookmark668)          | A string that specifies the ActionScript 2.0 class that will be associated with the symbol.                     |
| [item.linkageExportForAS](#_bookmark669)        | A Boolean value. If true, the item is exported for ActionScript.                                                |
| [item.linkageExportForRS](#_bookmark670)        | A Boolean value. If true, the item is exported for run-time sharing.                                            |
| [item.linkageExportInFirstFrame](#_bookmark671) | A Boolean value. If true, the item is exported in the first frame.                                              |
| [item.linkageIdentifier](#_bookmark672)         | A string that specifies the name Flash will use to identify the asset when linking to the destination SWF file. |
| [item.linkageImportForRS](#_bookmark673)        | A Boolean value. If true, the item is imported for run-time sharing.                                            |
| [item.linkageURL](#_bookmark674)                | A string that specifies the URL where the SWF file containing the shared asset is located.                      |
| [item.name](#_bookmark675)                      | A string that specifies the name of the library item, which includes the folder structure.                      |

<span id="item.addData()" class="anchor"></span>
