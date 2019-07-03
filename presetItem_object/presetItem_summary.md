## presetItem summary

#### Availability

Flash CS4 Professional.

#### Description

The presetItem object represents an item (preset or folder) in the Motion Presets panel (Window \Motion Presets). The array of presetItem objects is a property of the presetPanel object ([presetPanel.items](#_bookmark791)).
All properties of the presetItem object are read only. To perform tasks such as deleting, renaming, or moving items, use the methods of the [presetPanel object](#_bookmark779).

#### Property summary

You can use the following properties with the presetItem object:

| **Property**                                  | **Description**                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [presetItem.isDefault](#presetItem.isDefault) | Specifies whether the item is installed along with Flash or is a custom item that you or someone else has created. |
| [presetItem.isFolder](#_bookmark773)          | Specifies whether the item in the Motion Presets panel is a folder or a preset.                                    |
| [presetItem.level](#_bookmark774)             | The level of the item in the folder structure of the Motion Presets panel.                                         |
| [presetItem.name](#_bookmark775)              | The name of the preset or folder, without path information.                                                        |
| [presetItem.open](#_bookmark776)              | Specifies whether a folder in the Motion Presets panel is currently expanded.                                      |
| [presetItem.path](#_bookmark777)              | The path to the item in the Motion Presets panel folder tree, and the item name.                                   |

<span id="presetItem.isDefault" class="anchor"></span>

