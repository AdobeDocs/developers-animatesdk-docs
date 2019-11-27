## presetPanel.items

#### Availability

Flash CS4 Professional.

#### Usage

*presetPanel.items*

#### Description

Property; an array of presetItem objects in the Motion Presets panel (see [presetItem object](../presetItem_object/presetItem_summary.md)). Each item in the array represents either a folder or a preset.

#### Example

The following code displays the full pathnames of the items in the Motion Presets panel:

```javascript
var itemArray = fl.presetPanel.items; 
var length = itemArray.length
for (x=0; x<length; x++) { 
    fl.trace(itemArray[x].path);
}

```
#### See also

[presetPanel.getSelectedItems()](../presetPanel_object/presetPane7.md)
