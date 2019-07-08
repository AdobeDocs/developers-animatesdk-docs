## presetPanel.expandFolder()

#### Availability

Flash CS4 Professional.

#### Usage

presetPanel.expandFolder( \[bExpand \[, bRecurse \[, folderPath\] \] \] )

#### Parameters

**bExpand** A Boolean value that specifies whether to expand the folder (true) or collapse it (false). This parameter is optional; the default value is true.
**bRecurse** A Boolean value that specifies whether to expand or collapse the folder’s subfolders (true) or not false). This parameter is optional; the default value is false.
**folderPath** A string that specifies the path to the folder to expand or collapse. This parameter is optional.

#### Returns

A Boolean value of true if the folder or folders are successfully expanded or collapsed; false otherwise.

#### Description

Method; expands or collapses the currently selected folder or folders in the Motion Presets panel. To expand or collapse folders other than the folders that are currently selected, pass a value for *folderPath*.

#### Example

```javascript
The following example expands the Custom Presets folder but does not expand its subfolders:
fl.presetPanel.expandFolder(true, false, "Custom Presets");
The following example expands the Custom Presets folder and all its subfolders:
fl.presetPanel.expandFolder(true, true, "Custom Presets");

```