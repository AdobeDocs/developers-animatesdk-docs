## presetItem summary

#### Availability

Flash CS4 Professional.

#### Description

The presetItem object represents an item (preset or folder) in the Motion Presets panel (Window \Motion Presets). The array of presetItem objects is a property of the presetPanel object ([presetPanel.items](#!AdobeDocs/developers-animatesdk-docs/test/presetPanel_object/presetPane9.md)).
All properties of the presetItem object are read only. To perform tasks such as deleting, renaming, or moving items, use the methods of the [presetPanel object](#!AdobeDocs/developers-animatesdk-docs/test/presetPanel_object/presetPanel_summary.md).

#### Property summary

You can use the following properties with the presetItem object:

| **Property**                                  | **Description**                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [presetItem.isDefault](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetItem.md) | Specifies whether the item is installed along with Flash or is a custom item that you or someone else has created. |
| [presetItem.isFolder](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetIte1.md)          | Specifies whether the item in the Motion Presets panel is a folder or a preset.                                    |
| [presetItem.level](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetIte2.md)             | The level of the item in the folder structure of the Motion Presets panel.                                         |
| [presetItem.name](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetIte3.md)              | The name of the preset or folder, without path information.                                                        |
| [presetItem.open](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetIte4.md)              | Specifies whether a folder in the Motion Presets panel is currently expanded.                                      |
| [presetItem.path](#!AdobeDocs/developers-animatesdk-docs/test/presetItem_object/presetIte5.md)              | The path to the item in the Motion Presets panel folder tree, and the item name.                                   |

<span id="presetItem.isDefault" class="anchor"></span>

