## presetPanel.getSelectedItems()

#### Availability

Flash CS4 Professional.

#### Usage

presetPanel.getSelectedItems()

#### Parameters

None.

#### Returns

An array of presetItem objects.

#### Description

Method; returns an array of presetItem objects corresponding to the currently selected items in the Motion Presets panel (see [presetItem object](#_bookmark770)). Each item in the array represents either a folder or a preset.

#### Example

```
The following code displays the full pathnames of the currently selected items in the Motion Presets panel:
var itemArray = fl.presetPanel.getSelectedItems(); var length = itemArray.length
for (x=0; x\<length; x++) { fl.trace(itemArray\[x\].path);
}

```
#### See also

[presetPanel.items](#_bookmark790)
