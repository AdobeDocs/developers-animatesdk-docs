## item summary

#### Availability

Flash MX 2004.

#### Description

The Item object is an abstract base class. Anything in the library derives from Item. See also [library object](#!AdobeDocs/developers-animatesdk-docs/master/library_object/library_summary.md).

#### Method summary

The following methods are available for the Item object:

| **Method**                             | **Description**                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [item.addData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item.md))      | Adds specified data to a library item.                                                                                         |
| [item.getData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item1.md)        | Retrieves the value of the specified data.                                                                                     |
| [item.getPublishData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item2.md) | Indicates whether publishing of the specified persistent data is enabled for the specified format on a specified library item. |
| [item.hasData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item3.md)        | Determines whether the library item has the named data.                                                                        |
| [item.removeData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item14.md)     | Removes persistent data from the library item.                                                                                 |
| [item.setPublishData()](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item15.md) | Enables publishing of persistent data for a library item.                                                                      |

#### Property summary

The following properties are available for the Item object:

| **Property**                                    | **Description**                                                                                                 |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [item.itemType](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item4.md)                  | Read-only; a string that specifies the type of element.                                                         |
| [item.linkageBaseClass](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item5.md)          | A string that specifies the ActionScript 3.0 class that will be associated with the symbol.                     |
| [item.linkageClassName](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item6.md)          | A string that specifies the ActionScript 2.0 class that will be associated with the symbol.                     |
| [item.linkageExportForAS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item7.md)        | A Boolean value. If true, the item is exported for ActionScript.                                                |
| [item.linkageExportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item8.md)        | A Boolean value. If true, the item is exported for run-time sharing.                                            |
| [item.linkageExportInFirstFrame](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item9.md) | A Boolean value. If true, the item is exported in the first frame.                                              |
| [item.linkageIdentifier](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item10.md)         | A string that specifies the name Flash will use to identify the asset when linking to the destination SWF file. |
| [item.linkageImportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item11.md)        | A Boolean value. If true, the item is imported for run-time sharing.                                            |
| [item.linkageURL](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item12.md)                | A string that specifies the URL where the SWF file containing the shared asset is located.                      |
| [item.name](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item13.md)                      | A string that specifies the name of the library item, which includes the folder structure.                      |

<span id="item.addData()" class="anchor"></span>

