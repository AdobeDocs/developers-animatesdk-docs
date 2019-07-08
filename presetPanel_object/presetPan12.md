## presetPanel.renameItem()

#### Availability

Flash CS4 Professional.

#### Usage

presetPanel.renameItem(newName)

#### Parameters

**newName** A string that specifies the new name for the preset or folder.

#### Returns

A Boolean value of true if the preset or folder is successfully renamed; false otherwise.

#### Description

Method; renames the currently selected preset or folder to a specified name. This method succeeds only if a single preset or folder in the Custom Presets folder is selected. This method fails in the following situations:

-   No item is selected.

-   Multiple items are selected.

-   The selected item is in the Default Presets folder.

-   An item named *newName* exists in the same location as the selected item.

#### Example

```javascript
The following example renames the currently selected preset in the Custom Presets folder to Bounce Faster.
var renamed = fl.presetPanel.renameItem("Bounce Faster"); fl.trace(renamed);

```