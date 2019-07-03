## presetPanel.selectItem()

#### Availability

Flash CS4 Professional.

#### Usage

presetPanel.selectItem(namePath \[, bReplaceCurrentSelection \[, bSelect\] \])

#### Parameters

**namePath** A string that specifies the path and name of the item to select from the Motion Presets panel.
**bReplaceCurrentSelection** A Boolean value that specifies whether the specified item replaces any current selection (true) or is added to the current selection (false). This parameter is optional; the default value is true.
**bSelect** A Boolean value that specifies whether to select the item (true) or deselect the item (false). This parameter is optional; the default value is true. If you pass false for *bSelect*, the value of *bReplaceCurrentSelection* is ignored.

#### Returns

A Boolean value of true if the item was successfully selected or deselected; false otherwise.

#### Description

Method; selects or deselects an item in the Motion Presets panel, optionally replacing any items currently selected.

#### Example

```
The following code adds the fly-in-blur-right preset to the currently selected presets (if any) in the Motion Presets panel:
fl.presetPanel.selectItem("Default Presets/fly-in-blur-right", false);

```