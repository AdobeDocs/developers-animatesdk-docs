## presetItem.path

#### Availability

Flash CS4 Professional.

#### Usage

presetItem.path

#### Description

Read-only property: a string that represents the path to the item in the Motion Presets panel folder tree, and the item name.

#### Example

The following example illustrates the difference between the values in presetItem.name and presetItem.path.
```javascript
fl.outputPanel.clear();
var presetItemArray=fl.presetPanel.items;
for (i=0;i<presetItemArray.length; i++){
var presetItem = presetItemArray[i];
fl.trace("Name: " + presetItem.name + "\n" + "Path: " + presetItem.path);
fl.trace("");
}

```