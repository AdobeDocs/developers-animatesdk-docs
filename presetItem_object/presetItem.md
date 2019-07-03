## presetItem.isDefault

#### Availability

Flash CS4 Professional.

#### Usage

presetItem.isDefault

#### Description

Read-only property: a Boolean value that specifies whether the item is installed along with Flash (true) or is a custom item that you or someone else has created (false). If this value is true, you can consider it a “read-only” item; it can’t be moved, deleted, or have any similar operations applied to it.

#### Example

```
The following example displays the contents of the Motion Presets panel and indicates whether an item is installed along with Flash:
fl.outputPanel.clear();
var presetItemArray=fl.presetPanel.items; for (i=0;i\<presetItemArray.length; i++){
var presetItem = presetItemArray\[i\];
fl.trace(presetItem.name +", default =" + presetItem.isDefault);
}

```