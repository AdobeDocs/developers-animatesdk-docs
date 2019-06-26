## presetPanel.newFolder()

#### Availability

> Flash CS4 Professional.

#### Usage

> presetPanel.newFolder( \[folderPath\] )

#### Parameters

> **folderPath** A string that specifies where to add a new folder in the Motion Presets panel, and the name of the new folder. This parameter is optional.

#### Returns

> A Boolean value of true if the folder is successfully added; false otherwise.

#### Description

> Method; creates a folder in the folder tree of the Motion Presets panel. You can create only one new folder level with this method. That is, if you pass “Custom Presets/My First Folder/My Second Folder" for *folderPath*, “Custom Presets/My First Folder“ must exist in the folder tree.
>
> If you don’t pass a value for *folderPath*, a folder named “Untitled folder *n*” is created at the first level below “Custom Presets,” where *n* is incremented each time a folder is added in this fashion.
>
> ***Note:** You can’t add folders to the Default Presets folder.*

#### Example

> The following example adds a folder named Bouncing below the Custom Presets folder:
>
> fl.presetPanel.newFolder("Custom Presets/Bouncing");

#### See also

> [presetPanel.addNewItem()](#_bookmark781)
