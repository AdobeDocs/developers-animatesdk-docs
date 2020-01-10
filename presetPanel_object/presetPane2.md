## presetPanel.deleteFolder()

#### Availability

Flash CS4 Professional.

#### Usage

*presetPanel.deleteFolder( [folderPath])*

#### Parameters

**folderPath** A string that specifies the folder to delete from the Motion Presets panel. This parameter is optional.

#### Returns

A Boolean value of *true* if the folder or folders are successfully deleted; false otherwise.

#### Description

Method; deletes the specified folder and any of its subfolders from the folder tree of the Motion Presets panel. Any presets in the folders are also deleted. You can’t delete folders from the Default Presets folder.

If you don’t pass a value for *folderPath*, any folders that are currently selected are deleted.

***Note:** Folders are deleted without requesting user confirmation, and there is no way to undo this action.*

#### Example


The following code deletes a folder named Bouncing below the Custom Presets folder; any subfolders of Bouncing are also deleted:

```javascript
fl.presetPanel.deleteFolder("Custom Presets/Bouncing");

```
#### See also

[presetPanel.deleteItem()](../presetPanel_object/presetPane3.md)

<span id="presetPanel.deleteItem()" class="anchor"></span>
