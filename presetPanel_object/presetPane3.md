## presetPanel.deleteItem()

#### Availability

Flash CS4 Professional.

#### Usage

presetPanel.deleteItem( \[namePath\] )

#### Parameters

**namePath** A string that specifies the path and name of the item to delete from the Motion Presets panel. This parameter is optional.

#### Returns

A Boolean value of true if the item or items are successfully deleted; false otherwise.

#### Description

Method; deletes the specified preset from the Motion Presets panel. If you don’t pass a value for *namePath*, any presets that are currently selected are deleted. You can’t delete items from the Default Presets folder.
***Note:** Items are deleted without requesting user confirmation, and there is no way to undo this action.*

#### Example

```
The following code deletes a preset named aDribble from the Custom Presets folder:
fl.presetPanel.deleteItem("Custom Presets/aDribble");

```
#### See also

[presetPanel.deleteFolder()](#_bookmark783)
